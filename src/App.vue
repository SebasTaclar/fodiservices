<template>
  <header>
    <nav class="navbar">
      <RouterLink class="link-navbar home" to="/">FODISERVICES</RouterLink>

      <!-- Admin: Financiero, Operativo, Producto -->
      <RouterLink v-if="canAccessFinancieroRef" class="link-navbar" to="/financiero">Financiero</RouterLink>
      <RouterLink v-if="canAccessOperativoRef" class="link-navbar" to="/operativo">Operativo</RouterLink>
      <RouterLink v-if="canAccessProductoRef" class="link-navbar" to="/producto">Producto</RouterLink>

      <!-- Recursos Humanos: Todos los roles -->
      <RouterLink v-if="canAccessRecursosHumanosRef" class="link-navbar" to="/recursos-humanos">Recursos Humanos
      </RouterLink>

      <div class="nav-controls">
        <ThemeToggle />
        <RouterLink v-if="!isLoggedIn" class="link-navbar access" to="/login">Acceder</RouterLink>
        <span v-if="isLoggedIn" class="link-navbar access role-badge" :class="userRole">
          {{ userRole?.toUpperCase() }} - {{ username }}
        </span>
        <RouterLink v-if="isLoggedIn" @click="logout" class="link-navbar logout-btn" to="/">Cerrar sesión</RouterLink>
      </div>
    </nav>
  </header>

  <RouterView />
</template>

<script setup lang="ts">
import { RouterLink, RouterView, useRoute } from 'vue-router'
import {
  getTokenName,
  isTokenValid,
  userHasAdminRole,
  getUserRole,
  canAccessFinanciero,
  canAccessOperativo,
  canAccessProducto,
  canAccessRecursosHumanos,
  logout as authLogout
} from '@/utils/auth'
import { onMounted, ref, watch } from 'vue'
import router from './router'
import ThemeToggle from '@/components/ThemeToggle.vue'

const isLoggedIn = ref(false)
const username = ref('')
const isAdminRole = ref(false)
const userRole = ref('')

// Computed refs for permissions
const canAccessFinancieroRef = ref(false)
const canAccessOperativoRef = ref(false)
const canAccessProductoRef = ref(false)
const canAccessRecursosHumanosRef = ref(false)

const checkAuthStatus = () => {
  isLoggedIn.value = isTokenValid()
  if (isLoggedIn.value) {
    username.value = getTokenName() || ''
    userRole.value = getUserRole() || ''
    isAdminRole.value = userHasAdminRole()

    // Update permissions
    canAccessFinancieroRef.value = canAccessFinanciero()
    canAccessOperativoRef.value = canAccessOperativo()
    canAccessProductoRef.value = canAccessProducto()
    canAccessRecursosHumanosRef.value = canAccessRecursosHumanos()
  } else {
    username.value = ''
    userRole.value = ''
    isAdminRole.value = false
    canAccessFinancieroRef.value = false
    canAccessOperativoRef.value = false
    canAccessProductoRef.value = false
    canAccessRecursosHumanosRef.value = false
  }
}

const logout = () => {
  authLogout()
  isLoggedIn.value = false
  username.value = ''
  userRole.value = ''
  isAdminRole.value = false
  canAccessFinancieroRef.value = false
  canAccessOperativoRef.value = false
  canAccessProductoRef.value = false
  canAccessRecursosHumanosRef.value = false
  router.push('/')
}

onMounted(() => {
  checkAuthStatus()
})

const route = useRoute()
watch(route, () => {
  checkAuthStatus()
})
</script>

<style scoped>
.navbar {
  background-color: #031633;
  margin: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
  height: 60px;
  padding: 0 20px;
  box-shadow: 0 2px 10px rgba(255, 165, 0, 0.2);
}

.nav-controls {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-left: auto;
}

.link-navbar {
  text-decoration: none;
  padding: 10px;
  font-weight: 400;
  font-size: 1.2rem;
  color: #f0f0f0;
  transition: color 0.3s ease-in-out;
}

.link-navbar:hover {
  color: #FFA500;
  background-color: rgba(255, 165, 0, 0.1);
  border-radius: 50px;
}

.home {
  font-size: 1.5rem;
  color: #FFA500;
  font-weight: 1000;
}

.access {
  margin-left: 0;
}

.role-badge {
  background: linear-gradient(135deg, #FFA500 0%, #FFB733 100%);
  color: #031633;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-weight: 700;
  font-size: 0.9rem;
  border: 2px solid #FFA500;
}

.role-badge.admin {
  background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
  color: white;
  border-color: #e74c3c;
}

.role-badge.supervisor {
  background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
  color: white;
  border-color: #3498db;
}

.role-badge.employ {
  background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
  color: white;
  border-color: #2ecc71;
}

.logout-btn {
  background-color: rgba(231, 76, 60, 0.1);
  border: 1px solid #e74c3c;
  border-radius: 20px;
  padding: 0.5rem 1rem;
  transition: all 0.3s ease;
}

.logout-btn:hover {
  background-color: #e74c3c;
  color: white;
}

@media (max-width: 768px) {
  .navbar {
    flex-wrap: wrap;
    height: auto;
    padding: 10px;
  }

  .nav-controls {
    gap: 10px;
  }

  .link-navbar {
    font-size: 1rem;
    padding: 8px;
  }

  .home {
    font-size: 1.3rem;
  }
}
</style>
