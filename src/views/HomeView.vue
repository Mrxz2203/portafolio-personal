<template>
  <div class="page">

    <!-- ============================================================ -->
    <!-- NAVBAR                                                        -->
    <!-- ============================================================ -->
    <nav class="navbar">
      <div class="nav-logo">Sitio Web Personal</div>

      <button
        class="nav-toggle"
        :class="{ 'is-open': menuOpen }"
        @click="toggleMenu"
        :aria-expanded="menuOpen"
        aria-label="Abrir menú de navegación"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>

      <ul class="nav-links" :class="{ 'is-open': menuOpen }">
        <li v-for="link in navLinks" :key="link.id">
          <a
            :href="'#' + link.id"
            :class="{ active: activeSection === link.id }"
            @click="closeMenu"
          >{{ link.label }}</a>
        </li>
      </ul>
    </nav>

    <!-- ============================================================ -->
    <!-- SECCIONES                                                     -->
    <!-- ============================================================ -->
    <HeroSection />
    <AcercaSection />
    <PasatiemposSection />
    <SeriesSection />
    <SeriesFavoritasSection />
    <ProyectosSection />
    <BollywoodSection />

    <!-- ============================================================ -->
    <!-- FOOTER                                                        -->
    <!-- ============================================================ -->
    <footer id="footer" class="footer">
      <p>© 2026 <span class="accent-red">Jarold Gabriel</span> Garcia Cartagena </p>
    </footer>

    <!-- ============================================================ -->
    <!-- BOTÓN VOLVER ARRIBA                                           -->
    <!-- ============================================================ -->
    <button
      class="back-to-top"
      :class="{ 'is-visible': showBackToTop }"
      @click="scrollToTop"
      aria-label="Volver arriba"
    >
      ↑
    </button>

  </div>
</template>

<script>
import HeroSection from '@/components/sections/HeroSection.vue'
import AcercaSection from '@/components/sections/AcercaSection.vue'
import PasatiemposSection from '@/components/sections/PasatiemposSection.vue'
import SeriesSection from '@/components/sections/SeriesSection.vue'
import SeriesFavoritasSection from '@/components/sections/SeriesFavoritasSection.vue'
import ProyectosSection from '@/components/sections/ProyectosSection.vue'
import BollywoodSection from '@/components/sections/BollywoodSection.vue'

export default {
  name: 'HomeView',
  components: {
    HeroSection,
    AcercaSection,
    PasatiemposSection,
    SeriesSection,
    SeriesFavoritasSection,
    ProyectosSection,
    BollywoodSection
  },
  data() {
    return {
      menuOpen: false,
      activeSection: 'inicio',
      showBackToTop: false,
      navLinks: [
        { id: 'inicio', label: 'Inicio' },
        { id: 'acerca', label: 'Acerca de mí' },
        { id: 'pasatiempos', label: 'Pasatiempos' },
        { id: 'series', label: 'Series' },
        { id: 'series-favoritas', label: 'Series Favoritas' },
        { id: 'cartas', label: 'Cartas' },
        { id: 'bollywood', label: 'Bollywood' }
      ],
      spyObserver: null,
      revealObserver: null
    }
  },
mounted() {
    this.setupScrollSpy()
    this.setupRevealAnimations()
    this.revealVisibleOnLoad()
    window.addEventListener('scroll', this.handleScroll)
    this.handleScroll()
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
    if (this.spyObserver) this.spyObserver.disconnect()
    if (this.revealObserver) this.revealObserver.disconnect()
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen
    },
    closeMenu() {
      this.menuOpen = false
    },
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: 'smooth' })
    },
    handleScroll() {
      this.showBackToTop = window.scrollY > 500
    },
    // Revela de una las secciones que YA están a la vista al cargar la página
    // (caso: entrar directo con #ancla en la URL o refrescar a mitad de página,
    // donde nunca ocurre el "scroll" que el IntersectionObserver espera)
    revealVisibleOnLoad() {
      const sections = document.querySelectorAll('.page section:not(.hero)')
      sections.forEach((section) => {
        const rect = section.getBoundingClientRect()
        const enViewport = rect.top < window.innerHeight && rect.bottom > 0
        if (enViewport) {
          section.classList.add('is-visible')
          if (this.revealObserver) this.revealObserver.unobserve(section)
        }
      })
    },
    // Resalta el link del nav según la sección visible en pantalla
    setupScrollSpy() {
      const sections = document.querySelectorAll('.page section[id]')
      this.spyObserver = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              this.activeSection = entry.target.id
            }
          })
        },
        { rootMargin: '-40% 0px -55% 0px', threshold: 0 }
      )
      sections.forEach((section) => this.spyObserver.observe(section))
    },
    // Agrega la clase .is-visible (fade-in) la primera vez que una sección entra en viewport
    setupRevealAnimations() {
      const sections = document.querySelectorAll('.page section:not(.hero)')
      this.revealObserver = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              entry.target.classList.add('is-visible')
              this.revealObserver.unobserve(entry.target)
            }
          })
        },
        { threshold: 0.15 }
      )
      sections.forEach((section) => this.revealObserver.observe(section))
    }
  }
}
</script>

<!-- ================================================================ -->
<!-- CSS - Layout raíz: navbar (+ hamburguesa), footer, volver arriba -->
<!-- El resto vive en global.css o dentro de cada sección              -->
<!-- ================================================================ -->
<style scoped>
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

/* ---- LINK ACTIVO (scroll-spy) ---- */
.nav-links a.active { color: #FFFFFF; }
.nav-links a.active::after { width: 100%; background: #EF0107; }

/* ---- BOTÓN HAMBURGUESA (oculto en desktop) ---- */
.nav-toggle {
  display: none;
  flex-direction: column;
  justify-content: center;
  gap: 5px;
  width: 32px;
  height: 32px;
  background: transparent;
  border: none;
  cursor: pointer;
  z-index: 110;
}

.nav-toggle span {
  display: block;
  width: 100%;
  height: 2px;
  background: #FFFFFF;
  border-radius: 2px;
  transition: transform 0.3s, opacity 0.3s;
}

.nav-toggle.is-open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
.nav-toggle.is-open span:nth-child(2) { opacity: 0; }
.nav-toggle.is-open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

/* ---- FOOTER ---- */
.footer {
  text-align: center;
  padding: 2rem;
  border-top: 1px solid rgba(74,144,217,0.1);
  color: #A0AEC0;
  font-size: 0.9rem;
}

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

/* ---- BOTÓN VOLVER ARRIBA ---- */
.back-to-top {
  position: fixed;
  bottom: 2.5rem;
  right: 2.5rem;
  width: 56px;
  height: 56px;
  border-radius: 50%;
  border: 1px solid rgba(74,144,217,0.4);
  background: rgba(13,13,26,0.9);
  backdrop-filter: blur(8px);
  color: #4A90D9;
  font-size: 1.5rem;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  pointer-events: none;
  transform: translateY(10px);
  transition: opacity 0.3s, transform 0.3s, border-color 0.3s, background 0.3s;
  z-index: 90;
}

.back-to-top.is-visible {
  opacity: 1;
  pointer-events: auto;
  transform: translateY(0);
}

.back-to-top:hover {
  border-color: #EF0107;
  background: rgba(239,1,7,0.15);
  color: #FFFFFF;
}

@media (max-width: 768px) {
  .navbar { padding: 1rem 1.5rem; }

  .nav-toggle { display: flex; }

  .nav-links {
    position: fixed;
    top: 0;
    right: 0;
    height: 100vh;
    width: 70%;
    max-width: 280px;
    flex-direction: column;
    gap: 0;
    background: rgba(13,13,26,0.97);
    backdrop-filter: blur(12px);
    border-left: 1px solid rgba(74,144,217,0.15);
    padding: 6rem 2rem 2rem;
    transform: translateX(100%);
    transition: transform 0.35s ease;
    z-index: 105;
  }

  .nav-links.is-open { transform: translateX(0); }

  .nav-links li { width: 100%; }

  .nav-links a {
    display: block;
    padding: 0.9rem 0;
    font-size: 1.05rem;
    border-bottom: 1px solid rgba(74,144,217,0.1);
  }

  .back-to-top { bottom: 1.2rem; right: 1.2rem; width: 44px; height: 44px; }
}
</style>
