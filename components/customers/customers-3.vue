<template>
  <div class="container">
    <swiper class="swiper" ref="mySwiper" :options="swiperOptions">
      <swiper-slide>
        <div class="row justify-content-center py-5">
          <div class="col-12 col-md-8 col-6 text-center">
            <blockquote class="blockquote weight-500">“Les moments partagés avec Chantal ont été simplement bénissants. Elle m'a doucement guider dans mes réflexions et m'a aider à travailler sur moi-même. J'ai pu grâce à nos rencontre enfin apprendre à mieux me connaître, à m'aimer et enfin mettre mes limites. Douce, empathique, à l'écoute Chantal sait nous accompagné dans un respect des plus complet.”</blockquote>
            <p class="mb-0"><span class="weight-500">Alexandra,</span> en thérapie individuelle</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="row justify-content-center py-5">
          <div class="col-12 col-md-8 col-6 text-center">
            <blockquote class="blockquote weight-500">“Nous avons beaucoup apprécié les séances de coaching de couple avec Chantal, car elle sait très bien établir une ambiance propice aux échanges. La communication se fait sans jugement et dans le respect. Son approche permet également de créer des ponts qui favorisent l’ouverture, la compréhension et l’acceptation. Nous recommandons sans réserve Chantal à tous ceux qui veulent réellement améliorer leur relation de couple.”</blockquote>
            <p class="mb-0"><span class="weight-500">Véronique & Dany,</span> en thérapie de couple</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="row justify-content-center py-5">
          <div class="col-12 col-md-8 col-6 text-center">
            <blockquote class="blockquote weight-500">“Suite à certains problèmes dans ma vie, j'ai contacté Chantal pour m'aider à y voir plus clair. Tout de suite j'ai vu une différence. Je réussissais de plus en plus à analyser la situation par moi-même grâce aux outils qu'elle m'apportait. J'ai appris à prendre soin de moi, à accepter mes limites et à mieux accepter mes rechutes. Investir du temps et de l'énergie dans sa vie ce n'est pas toujours facile mais ça en vaut la peine. Avec Chantal c'est simple et facile de parler. Elle va à notre rythme tout en nous amenant plus loin dans notre vie. Je vous la recommande à 100%.”</blockquote>
            <p class="mb-0"><span class="weight-500">Myriam,</span> en thérapie individuelle</p>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="row justify-content-center py-5">
          <div class="col-12 col-md-8 col-6 text-center">
            <blockquote class="blockquote weight-500">“Chantal nous a aidé à avoir un but de couple tout en ayant des trucs pour les atteindre. Elle nous a appris à communiquer de façon efficace tout en restant dans le respect de l’autre et a se concentrer sur le NOUS…couple. Être focus sur le positif et ce que l'on aime  de l'autre tout en restant fixé  sur le nous. Elle nous guide dans nos moments plus difficile.”</blockquote>
            <p class="mb-0"><span class="weight-500">Suzy et Jocelyn,</span> en coaching de couple</p>
          </div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: 'customers-3',
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
      return {
        swiperOptions: {
          pagination: {
            el: '.swiper-pagination'
          }
        }
      }
    },
    computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },
    mounted() {
      console.log('Current Swiper instance object', this.swiper)
      this.swiper.slideTo(3, 1000, false)
    }
}
/*
var mySwiper = new Swiper('#slider-customers-3', {
    speed: 400,
    navigation: {
      nextEl: '#slider-customers-3-next',
      prevEl: '#slider-customers-3-prev',
    },
    pagination: {
      el: '#slider-customers-3-pagination',
      clickable: true
    }
  });
*/
</script>
