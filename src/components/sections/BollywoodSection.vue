<template>
  <section id="bollywood" class="bollywood">
    <div class="section-line"></div>
    <h2 class="section-title">Bollywood y su <span class="accent-red">influencia</span></h2>

    <div class="bolly-content">
      <div class="bolly-image-wrapper">
        <img src="@/assets/Bolly.png" alt="Sharukhan y Juhi Chawla" class="bolly-img" loading="lazy" />
        <div class="bolly-caption">Sharukhan y Juhi Chawla</div>
      </div>

      <div class="bolly-text">
        <p>
          ¿Cómo me adentre? Desde niño mi tío me hacía ver mil y una veces la filmografía de Sharukhan,
          tanto las películas como las canciones que eran populares en los años 90'' y 00'', con sus enseñanzas
          como profundizaciones en la toma de acciones tanto familiar como sentimental, aunque a veces se exageraba xd.
          Aún así, le tengo cariño por como me ayudaron a formar mis pensamientos y acciones que pese a mi pasado, ahora son marcados
          en mi presente, como el amar a alguien y como demostrarlo, a tus seres queridos, a ti mismo y a la vida efímera que tenemos.
        </p>
        <p>
          Siempre escucho que pueda las canciones que me marcaron, mi pareja favorita más que todo por la química es Sharukhan con
          Juhi Chawla, siendo ellos mejores amigos, películas como <span class="accent-red">Kabhi Haan Kabhi Naa </span>,
          <span class="accent-red">Mohhabatein</span>, <span class="accent-red">Dilwale Dulhania Le Jayenge</span>
          y <span class="accent-red">Kabhi Khushi Kabhie Gham</span> son mis favoritas.
        </p>
        <p>
          Eso sí, mi película como  canción favorita será
          <span class="accent-blue">Kal Ho Naa Ho</span>, por ser muy importante en mi vida.
        </p>
      </div>
    </div>

    <blockquote class="frase">
      "Vive al máximo cada momento, quizás no exista un mañana."
    </blockquote>
  </section>
</template>

<script>
export default {
  name: 'BollywoodSection'
}
</script>

<style scoped>
.bollywood {
  padding: 6rem 4rem;
  max-width: 1100px;
  margin: 0 auto;
}

.bolly-content {
  display: flex;
  gap: 3rem;
  align-items: flex-start;
  margin-top: 2rem;
}

.bolly-image-wrapper {
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.8rem;
}

.bolly-img {
  width: 260px;
  border-radius: 12px;
  border: 2px solid rgba(74,144,217,0.25);
  object-fit: cover;
  margin-bottom: 0.9rem;
}

.bolly-caption {
  background: linear-gradient(135deg, #EF0107, #001F5B);
  color: #FFFFFF;
  font-size: 0.85rem;
  font-weight: 600;
  padding: 0.5rem 1.2rem;
  border-radius: 50px;
  letter-spacing: 0.5px;
  text-align: center;
  margin-bottom: 1.5rem;
}

.bolly-text {
  border: 1px solid rgba(74,144,217,0.2);
  border-radius: 12px;
  padding: 1.8rem 2rem;
  background: rgba(255,255,255,0.03);
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}

.bolly-text p {
  color: #A0AEC0;
  font-size: 0.95rem;
  line-height: 1.8;
}

@media (max-width: 768px) {
  .bollywood { padding: 4rem 1.5rem; }
  .bolly-content { flex-direction: column; align-items: center; }
  .bolly-img { width: 100%; max-width: 320px; }
  .bolly-text { padding: 1.2rem; }
}
</style>
