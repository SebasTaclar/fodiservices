<template>
  <section id="servicios-fodiservices" class="services-section">
    <p class="section-title-1">Soluciones tecnológicas empresariales</p>
    <h2 class="section-title">NUESTROS SERVICIOS DE OUTSOURCING</h2>
    <div class="service-grid">
      <div class="service-card">
        <img src="/images/mainBanner1.jpg" alt="Desarrollo de Software">
        <h3>DESARROLLO DE SOFTWARE</h3>
        <p>Soluciones personalizadas para tu empresa</p>
      </div>
      <div class="service-card">
        <img src="/images/mainBanner2.png" alt="Consultoría IT">
        <h3>CONSULTORÍA IT</h3>
        <p>Asesoramiento tecnológico especializado</p>
      </div>
      <div class="service-card">
        <img src="/images/mainBanner3.jpg" alt="Soporte Técnico">
        <h3>SOPORTE TÉCNICO</h3>
        <p>Atención 24/7 para tu tranquilidad</p>
      </div>
    </div>
    <div class="service-grid">
      <div class="service-card">
        <img src="/images/andamio.png" alt="Infraestructura Cloud">
        <h3>INFRAESTRUCTURA CLOUD</h3>
        <p>Migración y gestión de servicios en la nube</p>
      </div>
      <div class="service-card">
        <img src="/images/GENERADORES2.png" alt="Seguridad Informática">
        <h3>SEGURIDAD INFORMÁTICA</h3>
        <p>Protección integral de tus sistemas</p>
      </div>
      <div class="service-card">
        <img src="/images/trompo.png" alt="Automatización">
        <h3>AUTOMATIZACIÓN DE PROCESOS</h3>
        <p>Optimización y digitalización empresarial</p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
defineOptions({
  name: 'OfferingsComponent',
});
</script>

<style scoped>
.services-section {
  background: #031633;
  padding: 60px 20px;
  text-align: center;
  font-family: 'Montserrat', sans-serif;
  color: white;
}

.section-title {
  font-size: 1.8rem;
  color: #ffffff;
  margin-bottom: 30px;
  text-transform: uppercase;
  font-weight: bold;
}

.section-title-1 {
  color: #ffffff;
  margin-bottom: 0px;
  text-transform: uppercase;
  font-weight: 10px;
}

.service-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
  margin-bottom: 50px;
}

.service-card {
  background: rgba(255, 255, 255, 0.932);
  width: 280px;
  border-radius: 15px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;
  overflow: hidden;
}

.service-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.25);
}

.service-card img {
  width: 100%;
  height: 170px;
  object-fit: cover;
}

.service-card h3 {
  margin: 15px 10px 5px;
  font-size: 1.1rem;
  color: #031633;
}

.service-card p {
  margin: 0 10px 15px;
  font-size: 0.95rem;
  color: #333;
}





.offerings {
  background-color: rgba(34, 34, 34, 0.9);
  height: 40vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 2rem;
  overflow: hidden;
}

.cards {
  display: flex;
  justify-content: center;
  gap: 3rem;
  height: 80%;
}

.card {
  border: 2px solid white;
  padding: 1rem;
  border-radius: 8px;
  color: rgb(19, 18, 18);
  text-align: left;
  cursor: pointer;
  font-size: 1rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  transition:
    background-color 0.3s,
    color 0.3s;
  width: 30%;
}

.rent {
  background-image: url('/images/rent_building_banner.png');
  background-size: cover;
}

.sell {
  background-image: url('/images/sell_tools_banner.png');
  background-size: contain;
}

.card h2 {
  margin: 0;
  font-family: 'Bricolage Grotesque', sans-serif;
}

.card p {
  margin: 0.5rem 0;
  font-family: 'Bricolage Grotesque', sans-serif;
}

.card:hover {
  background-color: rgba(23, 24, 26, 0.8);
  background-image: none;
  color: white;
}
</style>
