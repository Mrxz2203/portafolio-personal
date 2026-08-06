<template>
  <section id="acerca" class="acerca">
    <div class="section-line"></div>
    <h2 class="section-title">Acerca de <span class="accent-red">mí</span></h2>

    <div class="acerca-content">
      <div class="acerca-card">
        <div class="card-icon">🎓</div>
        <h3>Académico</h3>
        <p>Universitario de la carrera de Ingeniería de Sistemas, apasionado por la tecnología, programación, bases de datos y seguridad de la información.</p>
      </div>
      <div class="acerca-card highlight">
        <div class="card-icon">⚽</div>
        <h3>Deportivo</h3>
        <p>Amante del fútbol, hinchando por clubes como el <span class="accent-red">Fútbol Club Arsenal</span> de Inglaterra y <span class="accent-blue">Sporting Cristal</span> de Perú.</p>
      </div>
      <div class="acerca-card">
        <div class="card-icon">✍️</div>
        <h3>Creativo</h3>
        <p>Me encanta crear historias, poemas como canciones adaptables. Aspirante a futuro estudiante de Psicología (sueño frustrado) .</p>
      </div>
    </div>

    <blockquote class="frase">
      “Mi lema es luchar por mis sueños y no morir en el ‘hubiera’,
      sino en el éxito o en el fracaso de haberlo intentado.”
    </blockquote>

    <a href="#pasatiempos" class="scroll-down scroll-down-section">
      <span class="scroll-label">Sigue abajo</span>
      <div class="scroll-arrow">↓</div>
    </a>
  </section>
</template>

<script>
export default {
  name: 'AcercaSection'
}
</script>

<style scoped>
.acerca {
  padding: 6rem 4rem;
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.acerca-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-bottom: 3rem;
  width: 100%;
}

.acerca-card {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(74,144,217,0.15);
  border-radius: 16px;
  padding: 2rem;
  transition: transform 0.3s, border-color 0.3s;
}

.acerca-card:hover {
  transform: translateY(-6px);
  border-color: rgba(74,144,217,0.4);
}

.acerca-card.highlight {
  border-color: rgba(239,1,7,0.3);
  background: rgba(239,1,7,0.04);
}

.acerca-card.highlight:hover { border-color: rgba(239,1,7,0.6); }

.card-icon { font-size: 2rem; margin-bottom: 0.8rem; }

.acerca-card h3 {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 0.6rem;
  color: #FFFFFF;
}

.acerca-card p {
  font-size: 0.9rem;
  color: #A0AEC0;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .acerca { padding: 4rem 1.5rem; }
  .acerca-content { grid-template-columns: 1fr; }
}
</style>
