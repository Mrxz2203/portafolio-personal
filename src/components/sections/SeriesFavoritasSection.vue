<template>
  <section id="series-favoritas" class="series-favoritas">
    <div class="section-line section-line-center"></div>
    <h2 class="section-title section-title-center">Series <span class="accent-red">Favoritas</span></h2>

    <div class="series-grid">
      <div
        v-for="serie in seriesFavoritas"
        :key="serie.titulo"
        class="serie-card"
      >
        <div class="serie-img-wrapper">
          <img
            :src="getImg(serie.img)"
            :alt="serie.alt"
            class="serie-img"
            :style="serie.dim ? 'filter: brightness(0.7);' : ''"
            loading="lazy"
          />
        </div>
        <div class="serie-info">
          <h3>{{ serie.titulo }}</h3>
          <p>{{ serie.texto }}</p>
        </div>
      </div>
    </div>

    <a href="#series" class="scroll-down scroll-down-section">
      <span class="scroll-label">Sigue abajo</span>
      <div class="scroll-arrow">↓</div>
    </a>
  </section>
</template>

<script>
const imagenes = import.meta.glob('@/assets/*', { eager: true, import: 'default' })

export default {
  name: 'SeriesFavoritasSection',
  data() {
    return {
      seriesFavoritas: [
        { titulo: 'One Piece', img: 'One Piece.png', alt: 'One Piece', texto: 'Desde la trama hasta las enseñanzas fue lo que más me gusta de la serie. Demasiado por explayar, solo espero estar vivo cuando Luffy encuentre el One Piece y sea el Rey de los Piratas.' },
        { titulo: 'Shingeki no Kyojin', img: 'SNK.png', alt: 'Shingeki no Kyojin', texto: 'Pedazo de historia, lo disfrute como ninguna otra serie, cada arco, cada personaje y el final pues dejo a deber pero siempre fue un goce seguirlo durante años el manga.' },
        { titulo: 'Black Clover', img: 'Black Clover.jpg', alt: 'Black Clover', texto: 'Si algo admiro de la serie, es pese a todos sus altibajos y caída es que siempre me gusto pese al hate que tenía, Asta mi ídolo.' },
        { titulo: 'Dragon Ball Z', img: 'DBZ.png', alt: 'Dragon Ball Z', texto: 'Mi serie favorita y por lejos, mi infancia. Mi adolescnia, mi adultez y hasta siempre gracias Akira Toriyama.' },
        { titulo: 'Mentes Criminales', img: 'Criminal.png', alt: 'Mentes Criminales', texto: 'Las 12 primeras temporadas, y eso.. Disfrute viendo esta serie con cada tema o episodio que regía el máximo exponente de casos criminales. Guideon o Mattew los mejores.' },
        { titulo: 'The Walking Dead', img: 'TWD.png', alt: 'The Walking Dead', texto: 'Recuerdo haberlo visto teniendo 10 años pero me traumo, luego fue increible la aventura de Rick, las 6 primeras temporadas, fanatico de la serie.' },
        { titulo: 'Juego de Tronos', img: 'Tronos.jpg', alt: 'Juego de Tronos', texto: 'Las 6 primeras temporadas son un deleite visual como narrativo, las 7-8 no. Por cierto Jon Snow y Tyrion, los mejores.' },
        { titulo: 'Sangatsu no Lion', img: 'Sangatsu.png', alt: 'Sangatsu no Lion', texto: 'Rei soy yo, mentira, leanse el manga, me sentí muy representado con todo lo que lleva que siempre te pongan expectativas que tu no crees capaz de lograr mas si intentar.' },
        { titulo: 'Tokyo Ghoul', img: 'TokyoGhoul.jpg', alt: 'Tokyo Ghoul', texto: 'La primera serie como manga en la que me anime a leer desde el principio hasta el final, para mi el mejor seinen que he podido leer y disfrutar, gracias Ishida por todo. Yo también realmente estoy tan solo, Kaneki Ken.' },
        { titulo: 'Harry Potter', img: 'Potter.jpg', alt: 'Harry Potter', texto: 'La serie de películas lo disfruté desde niño. Cada año se estrenaba y era involvidable su mundo, los personajes como el desarrollo de estos en su crecimiento mientras yo también lo hacía. Aprecio cada cuan tiempo, viendo de nuevo la historia de Harry.' },
        { titulo: 'Re: Zero', img: 'ReZero.jpg', alt: 'Re: Zero', texto: 'Loco, te juro y menosprecie mucho a Subaru, más su trama y cómo conllevo su personalidad en un mundo tan distorsionado, te hace admiralo. Hoy siendo adulto disfruto su desarrollo esperando por un futuro sin preocupación para Subaru. PD: Tappei deja de hacer sufrir al muchacho.' },
        { titulo: 'Kaoru Hana wa Rin to Saku', img: 'KaoruHana.jpg', alt: 'Kaoru Hana wa Rin to Saku', texto: 'Esta serie es muy importante en mi vida de lo que debería ser. Amo a los protagonistas, Kaoru es un personaje tan hermosa como utópica y Rintaro es un chico increible en su determinacion tan increible, pero siempre que veo o sepa algo de esta hermosa serie, recuerdo a una persona muy importante, que le deseo lo mejor donde sea que ella esté.' },
        { titulo: 'Koe no Katachi', img: 'Katachi.png', alt: 'Koe no Katachi', dim: true, texto: 'Shouya me representó en mi punto más bajo de mi estabilidad emocional el como encomendo sus errores, aprendio de ellos para vivir con esa culpa y moldearla a un presente mejor. Lo que más admire de esta serie es que nuestros actos siempre tendrán consecuencias y en algun momento habrá que afrontarlas, le tengo un cariño a esta historia y su mensaje.' },
        { titulo: 'Kuso Onna ni Sachiare', img: 'Hope.png', alt: 'Kuso Onna ni Sachiare', dim: true, texto: 'Después de años encontre una historia muy entretenida, y ya era hora! Me encanta Sunao como protagonista, la amabilidad inherente que posee y su mentalidad al momento de afrontar y tomar las decisiones como consecuencias. Lemon hija mía te quiero, entiendo tus motivos, eres digna de admirar por la manera como seguiste adelante, pero hay formas de decidir, aun así espero ambos puedan afrontar el hecho de que una relación puede terminar por nuestra culpa y asumir nuestras consecuencias, son jóvenes y sus comunicaciones como el contexto de la historia se adhirio a mi en un momento vulnerable, espero verlos felices siendo ellos mismos, estando juntos o separados, la vida es así.' }
      ]
    }
  },
  methods: {
    getImg(nombre) {
      const entry = Object.entries(imagenes).find(([path]) => path.endsWith('/' + nombre))
      return entry ? entry[1] : ''
    }
  }
}
</script>

<style scoped>
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
  min-height: 160px;
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
  min-height: 160px;
  overflow: hidden;
  flex-shrink: 0;
}

.serie-img {
  width: 180px;
  height: 100%;
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
@media (max-width: 768px) {
  .series-favoritas { padding: 4rem 1.5rem; }
  .series-grid { grid-template-columns: 1fr; }
  .serie-card { flex-direction: column; min-height: auto; }
  .serie-img-wrapper {
    width: 100%;
    min-width: 100%;
    max-width: 100%;
    height: 180px;
    min-height: 180px;
  }
  .serie-img { width: 100%; }
}
</style>
