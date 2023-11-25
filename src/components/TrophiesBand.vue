<template>
  <div class="band desktop">
    <TrophyComponent v-for="(trophy, index) in trophies" :key="index"
        :amount="trophy.amount" :description="trophy.description">
      <img :src="trophy.img" alt="trophy"/>
    </TrophyComponent>
  </div>

  <section class="band mobile">
    <div class="swiper" ref="projectsSlider">
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide" v-for="(trophy, index) in trophies"
             :key="index">
              <TrophyComponent
                  :amount="trophy.amount" :description="trophy.description">
                <img :src="trophy.img" alt="trophy"/>
              </TrophyComponent>
        </div>
      </div>
      <!--        <div ref="btnLeft" class="swiper-button-prev "></div>-->
      <!--        <div ref="btnRight" class="swiper-button-next "></div>-->
    </div>
  </section>
</template>

<script setup lang="ts">

import Swiper from 'swiper';
import {Navigation} from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import {onMounted, ref} from "vue";
import TrophyComponent from "@/components/TrophyComponent.vue";

const projectsSlider = ref(null);
const btnLeft = ref(null);
const btnRight = ref(null);
onMounted(() => {
  const swiper = new Swiper(projectsSlider.value, {
    modules: [Navigation],
    slidesPerView: 2,
    spaceBetween: 10,
    // loop: true,
    navigation: {
      nextEl: btnRight.value,
      prevEl: btnLeft.value,
    },
  });
})

const trophies = [
  {
    amount: '',
    description: 'THE BEST CLUB OF THE 20TH CENTURY FIFA TROPHY',
    img: '/src/images/best.png',
  },
  {
    amount: '14',
    description: 'EUROPEAN CUPS',
    img: '/src/images/europeanCup.png',
  },
  {
    amount: '5',
    description: 'EUROPEAN SUPER CUPS',
    img: '/src/images/europeanSuperCup.png',
  },
  {
    amount: '2',
    description: 'UEFA CUPS',
    img: '/src/images/uefa.png',
  },
  {
    amount: '35',
    description: 'NATIONAL LEAGUES',
    img: '/src/images/laLiga.png',
  },
]

</script>

<style scoped lang="scss">

.band {
  width: 80%;
  margin-top: 10px;
}

.mobile {
  display: none;
  @media screen and (max-width: 400px) {
    display: flex;
    width: 90%;

    .swiper-slide {
      * {
        width: fit-content;
        height: fit-content;
      }
    }
  }
}

.desktop {
  display: flex;
  @media screen and (max-width: 400px) {
    display: none;
  }
}
</style>