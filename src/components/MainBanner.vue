<template>
  <section class="hero">
    <div class="hero-container">
      <!-- Lado izquierdo con contenido -->
      <div class="hero-content">
        <div class="hero-title">
          <h1>EXPERTOS EN</h1>
          <h1 class="highlight">OUTSOURCING</h1>
        </div>

        <div class="hero-tags">
          <span class="tag">INNOVATIVE DESIGN</span>
          <span class="tag">TECHNICAL EXPERTISE</span>
          <span class="tag">CLIENT-FOCUSED</span>
        </div>

        <div class="hero-contact">
          <div class="contact-item">
            <span class="icon">📞</span>
            <span>123-456-7890</span>
          </div>
          <div class="contact-item">
            <span class="icon">🌐</span>
            <span>www.fodiservices.com</span>
          </div>
          <div class="contact-item">
            <span class="icon">📍</span>
            <span>Bogotá-Colombia</span>
          </div>
        </div>
      </div>

      <!-- Lado derecho con imágenes circulares -->
      <div class="hero-visual">
        <div class="images-container">
          <div class="image-circle image-1">
            <img src="/images/mainBanner1.jpg" alt="FODISERVICES - Outsourcing profesional">
          </div>
          <div class="image-circle image-2">
            <img src="/images/mainBanner2.png" alt="FODISERVICES - Equipo experto">
          </div>
          <div class="image-circle image-3">
            <img src="/images/mainBanner3.jpg" alt="FODISERVICES - Soluciones innovadoras">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
/* Hero Section - Recreando el diseño exacto de la imagen */
.hero {
  min-height: 100vh;
  background-color: #031633;
  background-image:
    radial-gradient(circle, #FFA500 1px, transparent 1px),
    radial-gradient(circle, #FFA500 1px, transparent 1px);
  background-size: 50px 50px, 80px 80px;
  background-position: 0 0, 25px 25px;
  display: flex;
  align-items: center;
  font-family: 'Montserrat', sans-serif;
  overflow: hidden;
  position: relative;
}

.hero-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  width: 100%;
}

.hero-content {
  color: white;
  z-index: 2;
}

.hero-title {
  margin-bottom: 2rem;
}

.hero-title h1 {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.1;
  margin: 0;
  letter-spacing: -2px;
}

.hero-title .highlight {
  color: #FFA500;
  position: relative;
}

.hero-tags {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 2.5rem;
}

.tag {
  background-color: #FFA500;
  color: #031633;
  font-weight: 700;
  padding: 0.7rem 1.2rem;
  border-radius: 25px;
  font-size: 0.9rem;
  transition: all 0.3s ease;
  cursor: pointer;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.tag:hover {
  background-color: #E6940A;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(255, 165, 0, 0.4);
}

.hero-contact {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  font-size: 1.1rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.contact-item:hover {
  color: #FFA500;
  transform: translateX(8px);
}

.contact-item .icon {
  font-size: 1.3rem;
  width: 24px;
  text-align: center;
}

/* Lado derecho con imágenes circulares */
.hero-visual {
  position: relative;
  height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.images-container {
  position: relative;
  width: 100%;
  height: 100%;
}

.image-circle {
  position: absolute;
  border-radius: 50%;
  border: 5px solid #FFA500;
  overflow: hidden;
  box-shadow: 0 8px 32px rgba(255, 165, 0, 0.3);
  transition: all 0.4s ease;
}

.image-circle:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 40px rgba(255, 165, 0, 0.5);
  border-color: #FFB733;
}

.image-circle img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Posicionamiento específico de las imágenes */
.image-1 {
  width: 180px;
  height: 180px;
  top: 10%;
  left: 20%;
  animation: float1 6s ease-in-out infinite;
}

.image-2 {
  width: 200px;
  height: 200px;
  top: 15%;
  right: 10%;
  animation: float2 8s ease-in-out infinite;
}

.image-3 {
  width: 160px;
  height: 160px;
  bottom: 20%;
  left: 35%;
  animation: float3 7s ease-in-out infinite;
}

/* Animaciones de flotación */
@keyframes float1 {

  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }

  50% {
    transform: translateY(-20px) rotate(2deg);
  }
}

@keyframes float2 {

  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }

  50% {
    transform: translateY(-30px) rotate(-2deg);
  }
}

@keyframes float3 {

  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }

  50% {
    transform: translateY(-15px) rotate(1deg);
  }
}

/* Efectos adicionales */
.hero::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 50%;
  height: 100%;
  background: radial-gradient(circle at center,
      rgba(255, 165, 0, 0.1) 0%,
      transparent 70%);
  pointer-events: none;
}

.hero::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image:
    radial-gradient(circle, rgba(255, 165, 0, 0.15) 1px, transparent 1px);
  background-size: 30px 30px;
  background-position: 15px 15px;
  pointer-events: none;
  opacity: 0.3;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .hero-container {
    gap: 2rem;
  }

  .hero-title h1 {
    font-size: 2.8rem;
  }

  .image-1,
  .image-2,
  .image-3 {
    width: 140px;
    height: 140px;
  }

  .image-2 {
    width: 160px;
    height: 160px;
  }
}

@media (max-width: 768px) {
  .hero {
    min-height: auto;
    padding: 4rem 0;
  }

  .hero-container {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
  }

  .hero-title h1 {
    font-size: 2.2rem;
  }

  .hero-tags {
    justify-content: center;
  }

  .hero-contact {
    align-items: center;
  }

  .hero-visual {
    height: 400px;
  }

  .image-1 {
    top: 5%;
    left: 10%;
    width: 120px;
    height: 120px;
  }

  .image-2 {
    top: 10%;
    right: 5%;
    width: 140px;
    height: 140px;
  }

  .image-3 {
    bottom: 10%;
    left: 25%;
    width: 110px;
    height: 110px;
  }
}

@media (max-width: 480px) {
  .hero-container {
    padding: 0 1rem;
  }

  .hero-title h1 {
    font-size: 1.8rem;
  }

  .tag {
    padding: 0.5rem 1rem;
    font-size: 0.8rem;
  }

  .contact-item {
    font-size: 1rem;
  }

  .hero-visual {
    height: 300px;
  }

  .image-1,
  .image-2,
  .image-3 {
    width: 100px;
    height: 100px;
  }

  .image-2 {
    width: 120px;
    height: 120px;
  }
}
</style>
