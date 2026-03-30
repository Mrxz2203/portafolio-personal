<template>
  <div class="page">

    <!-- ============================================================ -->
    <!-- HTML - NAVBAR                                                 -->
    <!-- ============================================================ -->
    <nav class="navbar">
      <div class="nav-logo">Web Page Personal</div>
      <ul class="nav-links">
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#acerca">Acerca de mí</a></li>
        <li><a href="#pasatiempos">Pasatiempos</a></li>
        <li><a href="#series">Series</a></li>
        <li><a href="#series-favoritas">Series Favoritas</a></li>
        <li><a href="#cartas">Cartas</a></li>
      </ul>
    </nav>

    <!-- ============================================================ -->
    <!-- HTML - SECCIÓN: INICIO                                        -->
    <!-- ============================================================ -->
    <section id="inicio" class="hero">
      <div class="hero-glow-red"></div>
      <div class="hero-glow-blue"></div>

      <div class="hero-content">
        <div class="hero-text">
          <h1 class="nombre">
            <span class="accent-red">Jarold</span> Gabriel
          </h1>
          <h1 class="nombre">
            <span class="accent-red">Garcia</span> Cartagena
          </h1>
          <p class="subtitulo">Estudiante de Ingeniería de Sistemas</p>
          <a href="#acerca" class="btn-portafolio"> Web Personal</a>
        </div>

        <div class="hero-image-wrapper">
          <div class="image-ring"></div>
          <div class="image-ring ring-2"></div>
          <img src="@/assets/Rei.jpg" alt="Jarold Garcia" class="hero-img" />
          <div class="image-shadow"></div>
          <span class="deco-tag tag-1">JS</span>
          <span class="deco-tag tag-2">Vue</span>
          <span class="deco-tag tag-3">CSS</span>
        </div>
      </div>

      <a href="#acerca" class="scroll-down">
        <span class="scroll-label">Sigue abajo</span>
        <div class="scroll-arrow">↓</div>
      </a>
    </section>

    <!-- ============================================================ -->
    <!-- HTML - SECCIÓN: ACERCA DE MÍ                                 -->
    <!-- ============================================================ -->
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
          <p>Me encanta crear historias en textos o crear otro arquetipo a los poemas. Aspirante a futuro estudiante de Psicología.</p>
        </div>
      </div>

      <blockquote class="frase">
        “Mi meta principal es luchar por mis sueños y no morir en el ‘hubiera’, 
        sino en el éxito o en el fracaso de haberlo intentado.”
      </blockquote>

      <a href="#pasatiempos" class="scroll-down scroll-down-section">
        <span class="scroll-label">Sigue abajo</span>
        <div class="scroll-arrow">↓</div>
      </a>
    </section>

    <!-- ============================================================ -->
    <!-- HTML - SECCIÓN: PASATIEMPOS                                   -->
    <!-- ============================================================ -->
    <section id="pasatiempos" class="pasatiempos">
      <div class="section-line section-line-center"></div>
      <h2 class="section-title section-title-center">Pasa<span class="accent-red">tiempos</span></h2>

      <div class="hobbies-grid">
        <div class="hobby-card">
          <div class="hobby-img-wrapper">
            <img src="@/assets/Pasatiempo2.png" alt="Programacion" class="hobby-img" />
          </div>
          <div class="hobby-info">
            <h3>Programación</h3>
            <p>El poder mostrar lo que más te gusta en demostraciones es de lo mejor, este aspecto de sentirse uno mismo como lo es programar.</p>
          </div>
        </div>

        <div class="hobby-card">
          <div class="hobby-img-wrapper">
            <img src="@/assets/Pasatiempo3.jpg" alt="Fanatico de Futbol" class="hobby-img" />
          </div>
          <div class="hobby-info">
            <h3>Fanático de Fútbol</h3>
            <p>Solo a un desgraciado se le ocurre hinchar por clubes que te hacen sufrir todos los días, sin embargo es lo que más me representa, intentarlo hasta el final.</p>
          </div>
        </div>

        <div class="hobby-card">
          <div class="hobby-img-wrapper">
            <img src="@/assets/Pasatiempo1.jpg" alt="Player" class="hobby-img" />
          </div>
          <div class="hobby-info">
            <h3>Player</h3>
            <p>Me encanta Uma Musume por su manera de entablar relaciones y las historias de los caballos, te amo Nice Nature.
             Left 4 Dead el juego de mi infancia, F1 al que falla la insta.</p>
          </div>
        </div>

        <div class="hobby-card">
          <div class="hobby-img-wrapper">
            <img src="@/assets/Pasatiempo4.jpg" alt="Inspirador" class="hobby-img" />
          </div>
          <div class="hobby-info">
            <h3>Inspirador</h3>
            <p>Me encanta tocar la guitarra y siempre veo por cosas que me interesa hacer en el futuro como crear poemas.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ============================================================ -->
    <!-- HTML - AGREGA NUEVAS SECCIONES AQUÍ ARRIBA, ANTES DEL FOOTER -->
    <!-- ============================================================ -->
<!-- ============================================================ -->
<!-- HTML - SECCIÓN: SERIES                                        -->
<!-- ============================================================ -->
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
        continuación o de vez en cuando repito las series mil y una ves.
      </p>
      <p class="series-sub">Mis favoritos son:</p>
      <ul class="series-lista">
        <li>One Piece.</li>
        <li>Juego de Tronos.</li>
        <li>The Walking Dead.</li>
        <li>Black Clover.</li>
        <li>Dragon Ball Z.</li>
        <li>Shingeki no Kyojin.</li>
        <li>Kaoru Hana wa Rin to Saku.</li>
        <li>Tokyo Ghoul.</li>
        <li>Sangatsu no Lion.</li>
      </ul>
    </div>

    <div class="series-image-wrapper">
      <img src="@/assets/Luffy.png" alt="Luffy" class="series-img" />
      <div class="series-glow"></div>
    </div>

  </div>

  <a href="#footer" class="scroll-down scroll-down-section">
    <span class="scroll-label">Sigue abajo</span>
    <div class="scroll-arrow">↓</div>
  </a>
</section>
<!-- ============================================================ -->
<!-- HTML - SECCIÓN: SERIES FAVORITAS                             -->
<!-- ============================================================ -->
<section id="series-favoritas" class="series-favoritas">
  <div class="section-line section-line-center"></div>
  <h2 class="section-title section-title-center">Series <span class="accent-red">Favoritas</span></h2>

  <div class="series-grid">

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/One Piece.png" alt="One Piece" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>One Piece</h3>
        <p>Desde la trama hasta las enseñanzas fue lo que más me gusta de la serie. Demasiado por explayar, solo espero estar vivo cuando Luffy encuentre el One Piece y sea el Rey de los Piratas.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/SNK.png" alt="Shingeki no Kyojin" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Shingeki no Kyojin</h3>
        <p>Pedazo de historia, lo disfrute como ninguna otra serie, cada arco, cada personaje y el final pues dejo a deber pero siempre fue un goce seguirlo durante años el manga.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/Black Clover.jpg" alt="Black Clover" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Black Clover</h3>
        <p>Si algo admiro de la serie, es pese a todos sus altibajos y caída es que siempre me gusto pese al hate que tenía, Asta mi ídolo.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/DBZ.png" alt="Dragon Ball Z" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Dragon Ball Z</h3>
        <p>Mi serie favorita y por lejos, mi infancia. Mi adolescnia, mi adultez y hasta siempre gracias Akira Toriyama.</p>
      </div>
    </div>
<div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/Criminal.png" alt="Mentes Criminales" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Mentes Criminales</h3>
        <p>Las 12 primeras temporadas, y eso.. Disfrute viendo esta serie con cada tema o episodio que regía el máximo exponente de casos criminales. Guideon o Mattew los mejores.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/TWD.png" alt="The Walking Dead" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>The Walking Dead</h3>
        <p> Recuerdo haberlo visto teniendo 10 años pero me traumo, luego fue increible la aventura de Rick, las 6 primeras temporadas, fanatico de la serie</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/Tronos.jpg" alt="Juego de Tronos" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Juego de Tronos</h3>
        <p>Las 6 primeras temporadas son un deleite visual como narrativo, las 7-8 no. Por cierto Jon Snow y Tyrion, los mejores.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/Sangatsu.png" alt="Sangatsu no Lion" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Sangatsu no Lion</h3>
        <p>Rei soy yo, mentira, leanse el manga, me sentí muy representado con todo lo que lleva que siempre te pongan expectativas que tu no crees capaz de lograr mas si intentar.</p>
      </div>
    </div>
    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/Ken.png" alt="Tokyo Ghoul" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Tokyo Ghoul</h3>
        <p>La primera serie en la que me anime a leer desde el principio hasta el final, para mi el mejor seinen que he podido leer, gracias Ishida por todo. Realmente estoy tan solo, Kaneki Ken.</p>
      </div>
    </div>

    <div class="serie-card">
      <div class="serie-img-wrapper">
        <img src="@/assets/KaoruHana.jpg" alt="Kaoru Hana wa Rin to Saku" class="serie-img" />
      </div>
      <div class="serie-info">
        <h3>Kaoru Hana wa Rin to Saku</h3>
        <p>Esta serie es muy importante en mi vida de lo que debería ser. 
        Amo a los protagonistas, Kaoru es un personaje tan hermoso como utópico, Rintaro es un chico increible en su determinacion tan increible, como la historia, pero siempre que veo o sepa algo de esta hermosa serie,
         siempre recuerdo a aquella persona especial, una muy importante eternamente, que le deseo lo mejor donde sea que ella esté.</p>
      </div>
    </div>
  </div>

  <a href="#series" class="scroll-down scroll-down-section">
    <span class="scroll-label">Sigue abajo</span>
    <div class="scroll-arrow">↓</div>
  </a>
</section>
<!-- ============================================================ -->
<!-- HTML - SECCIÓN: PROYECTOS PERSONALES                         -->
<!-- ============================================================ -->
<section id="cartas" class="proyectos">
  <div class="section-line"></div>
  <h2 class="section-title">Mis cartas <span class="accent-red">personalizadas</span></h2>

  <div class="proyectos-grid">

    <a href="https://kiseki-green-gab.vercel.app/" target="_blank" class="proyecto-card">
      <div class="proyecto-img-wrapper">
        <img src="@/assets/Kiseki.png" alt="Kiseki" class="proyecto-img" />
        <div class="proyecto-overlay">
          <span class="proyecto-ver">Ver proyecto ↗</span>
        </div>
      </div>
      <div class="proyecto-info">
        <h3>Kiseki</h3>
      </div>
    
    </a>

    <a href="https://carta-amanecer.vercel.app/" target="_blank" class="proyecto-card">
      <div class="proyecto-img-wrapper">
        <img src="@/assets/Amanecer.png" alt="Más alla del Amanecer" class="proyecto-img" />
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
  <p><span class="nota-label">Dato:</span> Estas cartas son inspiradas en base a mis sentimientos y experiencias vividas de un mañana vivido.</p>
</div>
</section>
    <!-- ============================================================ -->
    <!-- HTML - FOOTER                                                 -->
    <!-- ============================================================ -->
  <footer class="footer">
      <p>© 2025 <span class="accent-red">Jarold</span> Garcia Cartagena — Vivo y muero por ti Claude </p>
      <a href="https://portafolio-gabriel-garcia.vercel.app/" target="_blank" class="btn-laboral">
        Portafolio Laboral
      </a>
    </footer>

  </div>
</template>

<!-- ================================================================ -->
<!-- JAVASCRIPT                                                        -->
<!-- Agrega imports, datos, funciones y lógica aquí                   -->
<!-- ================================================================ -->
<script>
export default {
  name: 'HomeView'

  // AGREGA NUEVAS PROPIEDADES O MÉTODOS AQUÍ ABAJO
}
</script>

<!-- ================================================================ -->
<!-- CSS                                                               -->
<!-- Agrega nuevos estilos al final, antes del cierre </style>        -->
<!-- ================================================================ -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Outfit:wght@300;400;600;700&display=swap');

* { margin: 0; padding: 0; box-sizing: border-box; }

.page {
  font-family: 'Outfit', sans-serif;
  background-color: #0D0D1A;
  color: #FFFFFF;
  scroll-behavior: smooth;
}

/* ---- NAVBAR ---- */
.navbar {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.2rem 4rem;
  background: rgba(13, 13, 26, 0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(74, 144, 217, 0.15);
}

.nav-logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.4rem;
  letter-spacing: 2px;
  color: #FFFFFF;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 2.5rem;
}

.nav-links a {
  color: #A0AEC0;
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 400;
  letter-spacing: 0.5px;
  transition: color 0.3s;
  position: relative;
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -4px; left: 0;
  width: 0; height: 2px;
  background: #EF0107;
  transition: width 0.3s;
}

.nav-links a:hover { color: #FFFFFF; }
.nav-links a:hover::after { width: 100%; }

/* ---- SECCIÓN: INICIO ---- */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 6rem 4rem 6rem;
}

.hero-glow-red {
  position: absolute;
  top: 20%; left: 5%;
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(239,1,7,0.12) 0%, transparent 70%);
  pointer-events: none;
}

.hero-glow-blue {
  position: absolute;
  bottom: 10%; right: 5%;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(74,144,217,0.10) 0%, transparent 70%);
  pointer-events: none;
}

.hero-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  max-width: 1100px;
  gap: 4rem;
}

.hero-text {
  flex: 1;
  animation: fadeInLeft 1s ease forwards;
}

@keyframes fadeInLeft {
  from { opacity: 0; transform: translateX(-40px); }
  to   { opacity: 1; transform: translateX(0); }
}

.nombre {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 5rem;
  line-height: 1.05;
  letter-spacing: 3px;
  color: #FFFFFF;
}

.accent-red  { color: #EF0107; }
.accent-blue { color: #4A90D9; }

.subtitulo {
  margin-top: 1rem;
  color: #A0AEC0;
  font-size: 1.1rem;
  font-weight: 300;
  letter-spacing: 1px;
}

.btn-portafolio {
  display: inline-block;
  margin-top: 2rem;
  padding: 0.8rem 2rem;
  background: linear-gradient(135deg, #EF0107, #001F5B);
  color: #FFFFFF;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  font-size: 0.95rem;
  letter-spacing: 1px;
  transition: transform 0.3s, box-shadow 0.3s;
  box-shadow: 0 4px 20px rgba(239,1,7,0.3);
}

.btn-portafolio:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 30px rgba(239,1,7,0.5);
}

.hero-image-wrapper {
  position: relative;
  flex-shrink: 0;
  animation: fadeInRight 1s ease forwards;
}

@keyframes fadeInRight {
  from { opacity: 0; transform: translateX(40px); }
  to   { opacity: 1; transform: translateX(0); }
}

.hero-img {
  width: 280px;
  height: 320px;
  object-fit: cover;
  border-radius: 16px;
  position: relative;
  z-index: 2;
  border: 2px solid rgba(74,144,217,0.3);
}

.image-ring {
  position: absolute;
  top: -15px; left: -15px;
  width: 310px; height: 350px;
  border: 2px solid rgba(239,1,7,0.3);
  border-radius: 20px;
  z-index: 1;
  animation: pulse 3s ease-in-out infinite;
}

.ring-2 {
  top: -28px; left: -28px;
  width: 336px; height: 376px;
  border-color: rgba(74,144,217,0.15);
  animation-delay: 1.5s;
}

@keyframes pulse {
  0%, 100% { opacity: 0.4; transform: scale(1); }
  50%       { opacity: 0.8; transform: scale(1.02); }
}

.image-shadow {
  position: absolute;
  bottom: -20px; left: 50%;
  transform: translateX(-50%);
  width: 200px; height: 30px;
  background: radial-gradient(ellipse, rgba(0,0,0,0.6) 0%, transparent 70%);
  z-index: 1;
}

.deco-tag {
  position: absolute;
  background: rgba(0,31,91,0.8);
  border: 1px solid rgba(74,144,217,0.5);
  color: #4A90D9;
  font-size: 0.75rem;
  font-weight: 700;
  padding: 0.3rem 0.7rem;
  border-radius: 20px;
  z-index: 3;
  letter-spacing: 1px;
}

.tag-1 { bottom: 40px; right: -30px; }
.tag-2 { top: 20px; right: -35px; color: #EF0107; border-color: rgba(239,1,7,0.5); background: rgba(91,0,0,0.5); }
.tag-3 { bottom: 90px; left: -35px; }

/* ---- FLECHA SCROLL ---- */
.scroll-down {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.4rem;
  text-decoration: none;
  position: absolute;
  bottom: 2rem;
  animation: bounce 2s infinite;
}

.scroll-down-section {
  position: relative;
  bottom: auto;
  margin-top: 3rem;
  animation: bounce 2s infinite;
}

.scroll-label {
  font-size: 0.7rem;
  letter-spacing: 2px;
  color: #A0AEC0;
  text-transform: uppercase;
}

.scroll-arrow {
  width: 40px; height: 40px;
  border: 2px solid rgba(74,144,217,0.5);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4A90D9;
  font-size: 1.1rem;
  transition: background 0.3s, border-color 0.3s;
}

.scroll-down:hover .scroll-arrow {
  background: rgba(74,144,217,0.15);
  border-color: #4A90D9;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50%       { transform: translateY(8px); }
}

/* ---- SECCIÓN: ACERCA DE MÍ ---- */
.acerca {
  padding: 6rem 4rem;
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.section-line {
  width: 60px; height: 3px;
  background: linear-gradient(to right, #EF0107, #4A90D9);
  border-radius: 2px;
  margin-bottom: 1rem;
}

.section-line-center {
  margin-left: auto;
  margin-right: auto;
}

.section-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3.5rem;
  letter-spacing: 3px;
  margin-bottom: 3rem;
  color: #FFFFFF;
}

.section-title-center {
  text-align: center;
  width: 100%;
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

.frase {
  border-left: 3px solid #EF0107;
  padding: 1rem 2rem;
  font-style: italic;
  color: #A0AEC0;
  font-size: 1rem;
  line-height: 1.8;
  background: rgba(239,1,7,0.04);
  border-radius: 0 8px 8px 0;
  width: 100%;
}

/* ---- SECCIÓN: PASATIEMPOS ---- */
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

/* ---- FOOTER ---- */
.footer {
  text-align: center;
  padding: 2rem;
  border-top: 1px solid rgba(74,144,217,0.1);
  color: #A0AEC0;
  font-size: 0.9rem;
}

/* ---- RESPONSIVE ---- */
@media (max-width: 768px) {
  .navbar { padding: 1rem 1.5rem; }
  .hero { padding: 6rem 1.5rem 6rem; }
  .hero-content { flex-direction: column; text-align: center; gap: 3rem; }
  .nombre { font-size: 3.5rem; }
  .acerca { padding: 4rem 1.5rem; }
  .pasatiempos { padding: 4rem 1.5rem; }
  .acerca-content { grid-template-columns: 1fr; }
  .hobbies-grid { grid-template-columns: 1fr; }
  .hobby-card { flex-direction: column; }
  .hobby-img-wrapper { width: 100%; height: 180px; }
}

/* ================================================================ */
/* AGREGA NUEVOS ESTILOS AQUÍ ABAJO        
                          */
/* ================================================================ */
/* ---- SECCIÓN: SERIES ---- */
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
/* ---- SECCIÓN: SERIES FAVORITAS ---- */
.series-favoritas {
  padding: 6rem 4rem;
  background: rgba(0,31,91,0.08);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.series-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  max-width: 1100px;
  width: 100%;
  margin: 0 auto;
}

.serie-card {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(74,144,217,0.15);
  border-radius: 16px;
  overflow: hidden;
  display: flex;
  flex-direction: row;
  align-items: stretch;
  height: 160px;
  transition: transform 0.3s, border-color 0.3s;
}

.serie-card:hover {
  transform: translateY(-6px);
  border-color: rgba(74,144,217,0.4);
}

.serie-img-wrapper {
  width: 180px;
  min-width: 180px;
  max-width: 180px;
  height: 160px;
  overflow: hidden;
  flex-shrink: 0;
}

.serie-img {
  width: 180px;
  height: 160px;
  object-fit: cover;
  display: block;
}

.serie-info {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 0.5rem;
  overflow: hidden;
}

.serie-info h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #FFFFFF;
}

.serie-info p {
  font-size: 0.85rem;
  color: #A0AEC0;
  line-height: 1.6;
}
/* ---- BOTÓN PORTAFOLIO LABORAL ---- */
.btn-laboral {
  display: inline-block;
  margin-top: 1rem;
  padding: 0.7rem 2rem;
  background: linear-gradient(135deg, #EF0107, #001F5B);
  color: #FFFFFF;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  font-size: 0.9rem;
  letter-spacing: 1px;
  transition: transform 0.3s, box-shadow 0.3s;
  box-shadow: 0 4px 20px rgba(239,1,7,0.3);
}

.btn-laboral:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 30px rgba(239,1,7,0.5);
}

/* ---- SECCIÓN: PROYECTOS PERSONALES ---- */
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

/* ---- NOTA PROYECTOS ---- */
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
