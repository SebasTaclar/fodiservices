<template>
 <div class="operativo-container">
  <div class="page-header">
   <h1>⚙️ MÓDULO OPERATIVO</h1>
   <p>Gestión operacional y procesos de FODISERVICES</p>
  </div>

  <div class="dashboard-grid">
   <div class="card">
    <div class="card-header">
     <h3>📋 Proyectos Activos</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">24</span>
      <span class="label">En progreso</span>
     </div>
     <div class="status-indicator active"></div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>✅ Proyectos Completados</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">156</span>
      <span class="label">Este año</span>
     </div>
     <div class="status-indicator completed"></div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>⏳ Pendientes</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">8</span>
      <span class="label">Por iniciar</span>
     </div>
     <div class="status-indicator pending"></div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>📊 Eficiencia</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">92%</span>
      <span class="label">Promedio</span>
     </div>
     <div class="progress-bar">
      <div class="progress" style="width: 92%"></div>
     </div>
    </div>
   </div>
  </div>

  <div class="operations-section">
   <div class="operations-card">
    <h3>🔄 Procesos Operativos</h3>
    <div class="process-list">
     <div class="process-item">
      <div class="process-icon">🏗️</div>
      <div class="process-info">
       <h4>Construcción de Software</h4>
       <p>Desarrollo y implementación de soluciones tecnológicas</p>
       <div class="process-status active">En Ejecución</div>
      </div>
     </div>

     <div class="process-item">
      <div class="process-icon">🔧</div>
      <div class="process-info">
       <h4>Mantenimiento de Sistemas</h4>
       <p>Soporte técnico y mantenimiento preventivo</p>
       <div class="process-status completed">Completado</div>
      </div>
     </div>

     <div class="process-item">
      <div class="process-icon">📱</div>
      <div class="process-info">
       <h4>Desarrollo Mobile</h4>
       <p>Aplicaciones móviles para iOS y Android</p>
       <div class="process-status pending">Planificado</div>
      </div>
     </div>

     <div class="process-item">
      <div class="process-icon">☁️</div>
      <div class="process-info">
       <h4>Migración a la Nube</h4>
       <p>Implementación de infraestructura cloud</p>
       <div class="process-status active">En Progreso</div>
      </div>
     </div>
    </div>
   </div>

   <div class="operations-card">
    <h3>📈 Métricas Operativas</h3>
    <div class="metrics-grid">
     <div class="metric-item">
      <span class="metric-number">98.5%</span>
      <span class="metric-label">Uptime</span>
     </div>
     <div class="metric-item">
      <span class="metric-number">4.2s</span>
      <span class="metric-label">Tiempo Respuesta</span>
     </div>
     <div class="metric-item">
      <span class="metric-number">99.1%</span>
      <span class="metric-label">Satisfacción Cliente</span>
     </div>
     <div class="metric-item">
      <span class="metric-number">24/7</span>
      <span class="metric-label">Soporte</span>
     </div>
    </div>
   </div>
  </div>
 </div>
</template>

<script setup lang="ts">
defineOptions({
 name: 'OperativoView',
});
</script>

<style scoped>
.operativo-container {
 padding: 2rem;
 padding-top: 80px;
 /* Offset para navbar fija */
 background-color: #f8f9fa;
 min-height: 100vh;
 font-family: 'Montserrat', sans-serif;
}

.page-header {
 text-align: center;
 margin-bottom: 3rem;
}

.page-header h1 {
 color: #031633;
 font-size: 2.5rem;
 font-weight: 800;
 margin-bottom: 0.5rem;
}

.page-header p {
 color: #666;
 font-size: 1.1rem;
}

.dashboard-grid {
 display: grid;
 grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
 gap: 2rem;
 margin-bottom: 3rem;
}

.card {
 background: white;
 border-radius: 12px;
 box-shadow: 0 4px 16px rgba(3, 22, 51, 0.1);
 overflow: hidden;
 transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
 transform: translateY(-4px);
 box-shadow: 0 8px 32px rgba(3, 22, 51, 0.15);
}

.card-header {
 background: linear-gradient(135deg, #031633 0%, #0a2a5c 100%);
 color: white;
 padding: 1.5rem;
}

.card-header h3 {
 margin: 0;
 font-size: 1.2rem;
 font-weight: 700;
}

.card-content {
 padding: 2rem;
 position: relative;
}

.metric {
 text-align: center;
 margin-bottom: 1rem;
}

.value {
 display: block;
 font-size: 2rem;
 font-weight: 800;
 color: #031633;
 margin-bottom: 0.5rem;
}

.label {
 color: #666;
 font-size: 0.9rem;
 text-transform: uppercase;
 letter-spacing: 0.5px;
}

.status-indicator {
 width: 12px;
 height: 12px;
 border-radius: 50%;
 position: absolute;
 top: 1rem;
 right: 1rem;
 animation: pulse 2s infinite;
}

.status-indicator.active {
 background-color: #28a745;
}

.status-indicator.completed {
 background-color: #007bff;
}

.status-indicator.pending {
 background-color: #ffc107;
}

@keyframes pulse {
 0% {
  opacity: 1;
 }

 50% {
  opacity: 0.5;
 }

 100% {
  opacity: 1;
 }
}

.progress-bar {
 width: 100%;
 height: 8px;
 background-color: #e9ecef;
 border-radius: 4px;
 overflow: hidden;
}

.progress {
 height: 100%;
 background: linear-gradient(90deg, #FFA500 0%, #FFB733 100%);
 border-radius: 4px;
 transition: width 0.5s ease;
}

.operations-section {
 display: grid;
 grid-template-columns: 2fr 1fr;
 gap: 2rem;
}

.operations-card {
 background: white;
 border-radius: 12px;
 box-shadow: 0 4px 16px rgba(3, 22, 51, 0.1);
 padding: 2rem;
}

.operations-card h3 {
 color: #031633;
 margin-bottom: 1.5rem;
 font-size: 1.3rem;
 font-weight: 700;
}

.process-list {
 display: flex;
 flex-direction: column;
 gap: 1.5rem;
}

.process-item {
 display: flex;
 align-items: center;
 gap: 1rem;
 padding: 1rem;
 border-radius: 8px;
 background-color: #f8f9fa;
 transition: all 0.3s ease;
}

.process-item:hover {
 background-color: #e9ecef;
 transform: translateX(4px);
}

.process-icon {
 font-size: 2rem;
 width: 60px;
 text-align: center;
}

.process-info {
 flex: 1;
}

.process-info h4 {
 margin: 0 0 0.5rem 0;
 color: #031633;
 font-size: 1.1rem;
 font-weight: 600;
}

.process-info p {
 margin: 0 0 0.5rem 0;
 color: #666;
 font-size: 0.9rem;
}

.process-status {
 display: inline-block;
 padding: 0.3rem 0.8rem;
 border-radius: 20px;
 font-size: 0.8rem;
 font-weight: 600;
 text-transform: uppercase;
}

.process-status.active {
 background-color: #d4edda;
 color: #155724;
}

.process-status.completed {
 background-color: #d1ecf1;
 color: #0c5460;
}

.process-status.pending {
 background-color: #fff3cd;
 color: #856404;
}

.metrics-grid {
 display: grid;
 grid-template-columns: 1fr 1fr;
 gap: 1.5rem;
}

.metric-item {
 text-align: center;
 padding: 1.5rem;
 border-radius: 8px;
 background: linear-gradient(135deg, #FFA500 0%, #FFB733 100%);
 color: white;
}

.metric-number {
 display: block;
 font-size: 1.8rem;
 font-weight: 800;
 margin-bottom: 0.5rem;
}

.metric-label {
 font-size: 0.9rem;
 text-transform: uppercase;
 letter-spacing: 0.5px;
}

@media (max-width: 768px) {
 .operativo-container {
  padding: 1rem;
 }

 .dashboard-grid {
  grid-template-columns: 1fr;
 }

 .operations-section {
  grid-template-columns: 1fr;
 }

 .metrics-grid {
  grid-template-columns: 1fr;
 }

 .page-header h1 {
  font-size: 2rem;
 }
}
</style>
