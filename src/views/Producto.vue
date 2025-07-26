<template>
 <div class="producto-container">
  <div class="page-header">
   <h1>🚀 MÓDULO PRODUCTO</h1>
   <p>Gestión de productos y desarrollo de FODISERVICES</p>
  </div>

  <div class="dashboard-grid">
   <div class="card">
    <div class="card-header">
     <h3>💼 Productos Activos</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">12</span>
      <span class="label">En producción</span>
     </div>
     <div class="product-indicator active"></div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>🔬 En Desarrollo</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">5</span>
      <span class="label">Proyectos</span>
     </div>
     <div class="product-indicator development"></div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>📊 Market Share</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">23%</span>
      <span class="label">Participación</span>
     </div>
     <div class="progress-bar">
      <div class="progress" style="width: 23%"></div>
     </div>
    </div>
   </div>

   <div class="card">
    <div class="card-header">
     <h3>⭐ Satisfacción</h3>
    </div>
    <div class="card-content">
     <div class="metric">
      <span class="value">4.8</span>
      <span class="label">Rating promedio</span>
     </div>
     <div class="stars">
      <span>⭐⭐⭐⭐⭐</span>
     </div>
    </div>
   </div>
  </div>

  <div class="products-section">
   <div class="products-card">
    <h3>🏆 Productos Destacados</h3>
    <div class="product-list">
     <div class="product-item">
      <div class="product-icon">💻</div>
      <div class="product-info">
       <h4>FODISERVICES ERP</h4>
       <p>Sistema integral de gestión empresarial</p>
       <div class="product-tags">
        <span class="tag">Enterprise</span>
        <span class="tag">Cloud</span>
        <span class="tag">AI-Powered</span>
       </div>
       <div class="product-status active">Activo</div>
      </div>
      <div class="product-metrics">
       <span class="metric-value">150+</span>
       <span class="metric-label">Clientes</span>
      </div>
     </div>

     <div class="product-item">
      <div class="product-icon">📱</div>
      <div class="product-info">
       <h4>FODI Mobile Suite</h4>
       <p>Aplicaciones móviles corporativas</p>
       <div class="product-tags">
        <span class="tag">Mobile</span>
        <span class="tag">Cross-Platform</span>
       </div>
       <div class="product-status development">En Desarrollo</div>
      </div>
      <div class="product-metrics">
       <span class="metric-value">75%</span>
       <span class="metric-label">Progreso</span>
      </div>
     </div>

     <div class="product-item">
      <div class="product-icon">🔒</div>
      <div class="product-info">
       <h4>FODI Security</h4>
       <p>Suite de seguridad cibernética</p>
       <div class="product-tags">
        <span class="tag">Security</span>
        <span class="tag">Blockchain</span>
       </div>
       <div class="product-status active">Activo</div>
      </div>
      <div class="product-metrics">
       <span class="metric-value">98.9%</span>
       <span class="metric-label">Efectividad</span>
      </div>
     </div>

     <div class="product-item">
      <div class="product-icon">🤖</div>
      <div class="product-info">
       <h4>FODI AI Assistant</h4>
       <p>Asistente inteligente para empresas</p>
       <div class="product-tags">
        <span class="tag">AI</span>
        <span class="tag">Machine Learning</span>
       </div>
       <div class="product-status beta">Beta</div>
      </div>
      <div class="product-metrics">
       <span class="metric-value">Beta</span>
       <span class="metric-label">Fase</span>
      </div>
     </div>
    </div>
   </div>

   <div class="roadmap-card">
    <h3>🗺️ Roadmap de Productos</h3>
    <div class="roadmap-timeline">
     <div class="timeline-item completed">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
       <h4>Q1 2025</h4>
       <p>Lanzamiento FODI ERP v3.0</p>
      </div>
     </div>

     <div class="timeline-item active">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
       <h4>Q2 2025</h4>
       <p>FODI Mobile Suite Beta</p>
      </div>
     </div>

     <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
       <h4>Q3 2025</h4>
       <p>AI Assistant Release</p>
      </div>
     </div>

     <div class="timeline-item">
      <div class="timeline-marker"></div>
      <div class="timeline-content">
       <h4>Q4 2025</h4>
       <p>FODI Security v2.0</p>
      </div>
     </div>
    </div>
   </div>
  </div>
 </div>
</template>

<script setup lang="ts">
defineOptions({
 name: 'ProductoView',
});
</script>

<style scoped>
.producto-container {
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

.product-indicator {
 width: 12px;
 height: 12px;
 border-radius: 50%;
 position: absolute;
 top: 1rem;
 right: 1rem;
 animation: pulse 2s infinite;
}

.product-indicator.active {
 background-color: #28a745;
}

.product-indicator.development {
 background-color: #FFA500;
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

.stars {
 text-align: center;
 font-size: 1.2rem;
}

.products-section {
 display: grid;
 grid-template-columns: 2fr 1fr;
 gap: 2rem;
}

.products-card,
.roadmap-card {
 background: white;
 border-radius: 12px;
 box-shadow: 0 4px 16px rgba(3, 22, 51, 0.1);
 padding: 2rem;
}

.products-card h3,
.roadmap-card h3 {
 color: #031633;
 margin-bottom: 1.5rem;
 font-size: 1.3rem;
 font-weight: 700;
}

.product-list {
 display: flex;
 flex-direction: column;
 gap: 1.5rem;
}

.product-item {
 display: grid;
 grid-template-columns: auto 1fr auto;
 gap: 1rem;
 padding: 1.5rem;
 border-radius: 8px;
 background-color: #f8f9fa;
 transition: all 0.3s ease;
}

.product-item:hover {
 background-color: #e9ecef;
 transform: translateY(-2px);
}

.product-icon {
 font-size: 2.5rem;
 width: 60px;
 text-align: center;
 align-self: center;
}

.product-info h4 {
 margin: 0 0 0.5rem 0;
 color: #031633;
 font-size: 1.1rem;
 font-weight: 600;
}

.product-info p {
 margin: 0 0 1rem 0;
 color: #666;
 font-size: 0.9rem;
}

.product-tags {
 display: flex;
 gap: 0.5rem;
 flex-wrap: wrap;
 margin-bottom: 0.5rem;
}

.tag {
 background-color: #FFA500;
 color: white;
 padding: 0.2rem 0.6rem;
 border-radius: 12px;
 font-size: 0.7rem;
 font-weight: 600;
 text-transform: uppercase;
}

.product-status {
 display: inline-block;
 padding: 0.3rem 0.8rem;
 border-radius: 20px;
 font-size: 0.8rem;
 font-weight: 600;
 text-transform: uppercase;
}

.product-status.active {
 background-color: #d4edda;
 color: #155724;
}

.product-status.development {
 background-color: #fff3cd;
 color: #856404;
}

.product-status.beta {
 background-color: #d1ecf1;
 color: #0c5460;
}

.product-metrics {
 text-align: center;
 align-self: center;
}

.metric-value {
 display: block;
 font-size: 1.5rem;
 font-weight: 800;
 color: #031633;
}

.metric-label {
 font-size: 0.8rem;
 color: #666;
 text-transform: uppercase;
}

.roadmap-timeline {
 position: relative;
}

.roadmap-timeline::before {
 content: '';
 position: absolute;
 left: 15px;
 top: 0;
 bottom: 0;
 width: 2px;
 background: linear-gradient(180deg, #FFA500 0%, #031633 100%);
}

.timeline-item {
 position: relative;
 padding-left: 3rem;
 margin-bottom: 2rem;
}

.timeline-marker {
 position: absolute;
 left: 7px;
 top: 5px;
 width: 16px;
 height: 16px;
 border-radius: 50%;
 background-color: #e9ecef;
 border: 3px solid #fff;
 box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.timeline-item.completed .timeline-marker {
 background-color: #28a745;
}

.timeline-item.active .timeline-marker {
 background-color: #FFA500;
 animation: pulse 2s infinite;
}

.timeline-content h4 {
 margin: 0 0 0.5rem 0;
 color: #031633;
 font-weight: 600;
}

.timeline-content p {
 margin: 0;
 color: #666;
 font-size: 0.9rem;
}

@keyframes pulse {
 0% {
  opacity: 1;
  transform: scale(1);
 }

 50% {
  opacity: 0.7;
  transform: scale(1.1);
 }

 100% {
  opacity: 1;
  transform: scale(1);
 }
}

@media (max-width: 768px) {
 .producto-container {
  padding: 1rem;
 }

 .dashboard-grid {
  grid-template-columns: 1fr;
 }

 .products-section {
  grid-template-columns: 1fr;
 }

 .product-item {
  grid-template-columns: 1fr;
  text-align: center;
 }

 .page-header h1 {
  font-size: 2rem;
 }
}
</style>
