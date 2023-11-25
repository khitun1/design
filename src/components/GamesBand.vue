<template>
  <div class="band desktop">
    <button class="prev">
      <img src="../images/prev.png" alt="prev button">
    </button>
    <div class="matches">
      <GameComponent v-for="(game, index) in games" :key="index"
          :score="game.score" :first-half="game.half" :cur="game.cur"
      >
        <img v-for="(img, index) in game.img" :key="index"
             :src="img" alt="logo"/>
      </GameComponent>
    </div>
    <button class="next">
      <img src="../images/next.png" alt="next button">
    </button>
  </div>

  <section class="band mobile">
    <div class="swiper" ref="projectsSlider">
      <div ref="btnLeft" class="swiper-button-prev "></div>
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide matches" v-for="(game, index) in games"
             :key="index">
          <GameComponent
                         :score="game.score"
                         :first-half="game.half"
                         :cur="game.cur"
          >
            <img v-for="(img, index) in game.img" :key="index"
                 :src="img" alt="logo"/>
          </GameComponent>
        </div>
      </div>
              <div ref="btnRight" class="swiper-button-next "></div>
    </div>
  </section>
</template>

<script setup lang="ts">
import GameComponent from "@/components/GameComponent.vue";
import Swiper from 'swiper';
import {Navigation} from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import {onMounted, ref} from "vue";

const projectsSlider = ref(null);
const btnLeft = ref(null);
const btnRight = ref(null);
onMounted(() => {
  const swiper = new Swiper(projectsSlider.value, {
    modules: [Navigation],
    slidesPerView: 3,
    spaceBetween: 5,
    initialSlide: 2,
    // loop: true,
    navigation: {
      nextEl: btnRight.value,
      prevEl: btnLeft.value,
    },
  });
})

const games = [
  {
    score: '0 : 3',
    half: '(0:2)',
    img: [
        '/src/images/girona.png',
        '/src/images/real.png',
    ]
  },
  {
    score: '2 : 3',
    half: '(1:2)',
    img: [
      '/src/images/napoli.png',
      '/src/images/real.png',
    ]
  },
  {
    score: '4 : 0',
    half: '(1:0)',
    img: [
      'src/images/real.png',
      'src/images/osasuna.png',
    ]
  },
  {
    score: '7 D 8 H 30 M',
    half: 'Sat, 21/10 ',
    cur: true,
    img: [
      'src/images/sevilla.png',
      'src/images/real.png',
    ]
  },
  {
    score: 'Tue, 24/10',
    half: '22:00 GMT+5',
    img: [
      'src/images/Braga.png',
      'src/images/real.png',
    ]
  },
  {
    score: 'Sat, 28/10',
    half: '17:35 GMT+5',
    img: [
      'src/images/barcelona.png',
      'src/images/real.png',
    ]
  },
  {
    score: 'Sun, 05/11',
    half: '23:00 GMT+5',
    img: [
      'src/images/real.png',
      'src/images/rayo.png',
    ]
  },

]

</script>

<style scoped lang="scss">

.matches {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  @media screen and (max-width: 400px) {

    img {
      width: 40%;
      height: 40%;
    }
  }

}

.band {
  display: flex;
  width: 85%;
  margin-bottom: 10px;
}

.prev, next {
  background: none;
  border: none;
  cursor: pointer;
}

.swiper-button-prev {
  color: transparent;
  background-image: url("../images/prev.png");
  margin-left: -10px;
}

.swiper-button-next {
  color: transparent;
  background-image: url("../images/next.png");
  margin-right: -15px;
}

.mobile {
  display: none;
  @media screen and (max-width: 400px) {
    display: flex;
  }
}

.desktop {
  display: flex;
  @media screen and (max-width: 400px) {
    display: none;
  }
}

</style>