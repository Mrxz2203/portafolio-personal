<template>
  <section id="series" class="series">
    <div class="series-content">

      <div class="series-text">
        <h2 class="series-title">
          Creiste que me olvidaria de mis
          <span class="accent-blue">Series</span>?
        </h2>
        <p class="series-intro">
          Ver los animes como series en su momento fue lo que más me rescató de
          algunos problemas personales, así que siempre que puedo veo su
          continuación o repito su historia para disfrutarlo como un niño esperando sonreír.
        </p>
        <p class="series-sub">Mis favoritos son:</p>
        <ul class="series-lista">
          <li>One Piece.</li>
          <li>Juego de Tronos.</li>
          <li>The Walking Dead.</li>
          <li>Black Clover.</li>
          <li>Dragon Ball Z.</li>
<li>Mentes Criminales.</li>
<li>Shingeki no Kyojin.</li>
          <li>Kaoru Hana wa Rin to Saku.</li>
          <li>Tokyo Ghoul.</li>
          <li>Sangatsu no Lion.</li>
          <li>Re:Zero kara Hajimeru Isekai Seikatsu.</li>
          <li>Harry Potter.</li>
          <li>Koe no Katachi.</li>
          <li>Kuso Onna ni Sachiare.</li>
        </ul>
      </div>

      <div class="series-image-wrapper">
        <img src="@/assets/Luffy.png" alt="Luffy" class="series-img" loading="lazy" />
        <div class="series-glow"></div>
      </div>

    </div>

    <a href="#footer" class="scroll-down scroll-down-section">
      <span class="scroll-label">Sigue abajo</span>
      <div class="scroll-arrow">↓</div>
    </a>
  </section>
</template>

<script>
export default {
  name: 'SeriesSection'
}
</script>

<style scoped>
.series {
  padding: 6rem 4rem;
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.series-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 4rem;
  width: 100%;
}

.series-text {
  flex: 1;
}

.series-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 4rem;
  line-height: 1.1;
  letter-spacing: 2px;
  color: #FFFFFF;
  margin-bottom: 2rem;
}

.series-intro {
  color: #A0AEC0;
  font-size: 0.95rem;
  line-height: 1.7;
  margin-bottom: 1rem;
}

.series-sub {
  color: #FFFFFF;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.series-lista {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}

.series-lista li {
  color: #A0AEC0;
  font-size: 0.95rem;
  padding-left: 1rem;
  position: relative;
}

.series-lista li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #EF0107;
}

.series-image-wrapper {
  position: relative;
  flex-shrink: 0;
}

.series-img {
  width: 320px;
  object-fit: contain;
  position: relative;
  z-index: 2;
  filter: drop-shadow(0 20px 40px rgba(74,144,217,0.3));
}

.series-glow {
  position: absolute;
  bottom: 0; left: 50%;
  transform: translateX(-50%);
  width: 250px; height: 40px;
  background: radial-gradient(ellipse, rgba(74,144,217,0.4) 0%, transparent 70%);
  z-index: 1;
}

@media (max-width: 768px) {
  .series { padding: 4rem 1.5rem; }
  .series-content { flex-direction: column-reverse; text-align: center; }
  .series-title { font-size: 2.8rem; }
  .series-img { width: 220px; }
  .series-lista li { text-align: left; }
}
</style>
