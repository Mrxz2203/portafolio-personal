<template>
  <section id="cartas" class="proyectos">
    <div class="section-line"></div>
    <h2 class="section-title">Mis cartas <span class="accent-red">personalizadas</span></h2>

    <div class="proyectos-grid">

      <a href="https://kiseki-green-gab.vercel.app/" target="_blank" class="proyecto-card">
        <div class="proyecto-img-wrapper">
          <img src="@/assets/Kiseki.png" alt="Kiseki" class="proyecto-img" loading="lazy" />
          <div class="proyecto-overlay">
            <span class="proyecto-ver">Ver proyecto ↗</span>
          </div>
        </div>
        <div class="proyecto-info">
          <h3>Milagro</h3>
        </div>
      </a>

      <a href="https://carta-amanecer.vercel.app/" target="_blank" class="proyecto-card">
        <div class="proyecto-img-wrapper">
          <img src="@/assets/Amanecer.png" alt="Más alla del Amanecer" class="proyecto-img" loading="lazy" />
          <div class="proyecto-overlay">
            <span class="proyecto-ver">Ver proyecto ↗</span>
          </div>
        </div>
        <div class="proyecto-info">
          <h3>Carta Amanecer</h3>
        </div>
      </a>

    </div>
    <div class="proyecto-nota">
      <span class="nota-icono">👁️</span>
      <p><span class="nota-label">Dato:</span> Estos programas fueron inspiradas en base a mis sentimientos de una experiencia vivida. Asimismo, me gustaron las canciones de Green.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProyectosSection'
}
</script>

<style scoped>
.proyectos {
  padding: 6rem 4rem;
  max-width: 1100px;
  margin: 0 auto;
}

.proyectos-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.proyecto-card {
  text-decoration: none;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid rgba(74,144,217,0.15);
  background: rgba(255,255,255,0.03);
  transition: transform 0.3s, border-color 0.3s;
  display: block;
}

.proyecto-card:hover {
  transform: translateY(-6px);
  border-color: rgba(74,144,217,0.4);
}

.proyecto-img-wrapper {
  position: relative;
  width: 100%;
  height: 220px;
  overflow: hidden;
}

.proyecto-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s;
}

.proyecto-card:hover .proyecto-img {
  transform: scale(1.05);
}

.proyecto-overlay {
  position: absolute;
  inset: 0;
  background: rgba(13,13,26,0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s;
}

.proyecto-card:hover .proyecto-overlay {
  opacity: 1;
}

.proyecto-ver {
  color: #FFFFFF;
  font-weight: 700;
  font-size: 1rem;
  letter-spacing: 1px;
  border: 2px solid #FFFFFF;
  padding: 0.5rem 1.5rem;
  border-radius: 50px;
}

.proyecto-info {
  padding: 1.2rem 1.5rem;
}

.proyecto-info h3 {
  color: #FFFFFF;
  font-size: 1.1rem;
  font-weight: 700;
}

@media (max-width: 768px) {
  .proyectos { padding: 4rem 1.5rem; }
  .proyectos-grid { grid-template-columns: 1fr; }
}

.proyecto-nota {
  display: flex;
  align-items: flex-start;
  gap: 0.8rem;
  margin-top: 2rem;
  padding: 1rem 1.5rem;
  background: rgba(74,144,217,0.06);
  border: 1px solid rgba(74,144,217,0.2);
  border-radius: 10px;
}

.nota-icono {
  font-size: 1.2rem;
  flex-shrink: 0;
  margin-top: 0.1rem;
}

.proyecto-nota p {
  color: #A0AEC0;
  font-size: 0.9rem;
  line-height: 1.6;
  font-style: italic;
}

.nota-label {
  color: #4A90D9;
  font-weight: 700;
  font-style: normal;
}
</style>
