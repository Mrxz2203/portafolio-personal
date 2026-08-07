<template>
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
        <p class="subtitulo">Estudiante de Ingeniería de Sistemas de Información.</p>
        <a href="#acerca" class="btn-portafolio"> Sitio Web Personal</a>
      </div>

      <div class="hero-image-wrapper">
        <div class="image-ring"></div>
        <div class="image-ring ring-2"></div>
        <img src="@/assets/catpfp.jpg" alt="Gabriel Garcia" class="hero-img" />
        <div class="image-shadow"></div>
        <span class="deco-tag tag-1">JS</span>
        <span class="deco-tag tag-2">Vue</span>
        <span class="deco-tag tag-3">CSS</span>
        <span class="deco-tag tag-4">React</span>
      </div>
    </div>

    <a href="#acerca" class="scroll-down">
      <span class="scroll-label">Sigue abajo</span>
      <div class="scroll-arrow">↓</div>
    </a>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
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
.tag-4 { top: 90px; left: -40px; }
@media (max-width: 768px) {
  .hero { padding: 6rem 1.5rem 6rem; }
  .hero-content { flex-direction: column; text-align: center; gap: 3rem; }
  .nombre { font-size: 3.5rem; }
}
</style>
