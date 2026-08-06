<template>
  <section id="pasatiempos" class="pasatiempos">
    <div class="section-line section-line-center"></div>
    <h2 class="section-title section-title-center">Pasa<span class="accent-red">tiempos</span></h2>

    <div class="hobbies-grid">
      <div class="hobby-card">
        <div class="hobby-img-wrapper">
          <img src="@/assets/progra.png" alt="Programacion" class="hobby-img" loading="lazy" />
        </div>
        <div class="hobby-info">
          <h3>Programación</h3>
          <p>El poder mostrar lo que más te gusta en demostraciones es de lo mejor, este aspecto de sentirse uno mismo como lo es programar.</p>
        </div>
      </div>

      <div class="hobby-card">
        <div class="hobby-img-wrapper">
          <img src="@/assets/Pasatiempo3.jpg" alt="Fanatico de Futbol" class="hobby-img" loading="lazy" />
        </div>
        <div class="hobby-info">
          <h3>Fanático de Fútbol</h3>
          <p>Solo a un desgraciado se le ocurre hinchar por clubes que te hacen sufrir todos los días, sin embargo es lo que más me representa, intentarlo hasta el final.</p>
        </div>
      </div>

      <div class="hobby-card">
        <div class="hobby-img-wrapper">
          <img src="@/assets/Pasatiempo1.jpg" alt="Player" class="hobby-img" loading="lazy" />
        </div>
        <div class="hobby-info">
          <h3>Player</h3>
          <p>Me encanta Uma Musume por su manera de entablar relaciones y las historias de los caballos, te amo Nice Nature.
           Left 4 Dead el juego de mi infancia, F1 al que falla la insta.</p>
        </div>
      </div>

      <div class="hobby-card">
        <div class="hobby-img-wrapper">
          <img src="@/assets/Pasatiempo4.jpg" alt="Inspirador" class="hobby-img" loading="lazy" />
        </div>
        <div class="hobby-info">
          <h3>Inspirador</h3>
          <p>Me encanta tocar la guitarra y siempre veo por cosas que me interesa hacer en el futuro como crear poemas.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PasatiemposSection'
}
</script>

<style scoped>
.pasatiempos {
  background: rgba(0,31,91,0.08);
  padding: 6rem 4rem;
}

.hobbies-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  max-width: 1100px;
  margin: 0 auto;
}

.hobby-card {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(74,144,217,0.15);
  border-radius: 16px;
  overflow: hidden;
  display: flex;
  flex-direction: row;
  transition: transform 0.3s, border-color 0.3s;
}

.hobby-card:hover {
  transform: translateY(-6px);
  border-color: rgba(74,144,217,0.4);
}

.hobby-img-wrapper {
  width: 180px;
  flex-shrink: 0;
}

.hobby-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.hobby-info {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 0.5rem;
}

.hobby-info h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #FFFFFF;
}

.hobby-info p {
  font-size: 0.85rem;
  color: #A0AEC0;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .pasatiempos { padding: 4rem 1.5rem; }
  .hobbies-grid { grid-template-columns: 1fr; }
  .hobby-card { flex-direction: column; }
  .hobby-img-wrapper { width: 100%; height: 180px; }
}
</style>
