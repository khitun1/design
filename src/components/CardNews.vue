<template>
  <div class="news desktop">
    <CardComponent v-for="(card, index) in cards" :key="index"
        :title="card.title"
        :text="card.text"
    >
      <img :src="card.img" alt="picture"/>
    </CardComponent>
  </div>

  <section class="news mobile">
      <div class="swiper" ref="projectsSlider">
        <!-- Additional required wrapper -->
        <div class="swiper-wrapper">
          <!-- Slides -->
          <div class="swiper-slide" v-for="(card, index) in cards"
               :key="index">
                <CardComponent
                    :title="card.title"
                    :text="card.text"
                >
                  <img :src="card.img" alt="picture"/>
                </CardComponent>
          </div>
        </div>
<!--        <div ref="btnLeft" class="swiper-button-prev "></div>-->
<!--        <div ref="btnRight" class="swiper-button-next "></div>-->
      </div>
  </section>
</template>

<script setup>
import Swiper from 'swiper';
import {Navigation} from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import {onMounted, ref} from "vue";
import CardComponent from "@/components/CardComponent.vue";

const projectsSlider = ref(null);
const btnLeft = ref(null);
const btnRight = ref(null);
onMounted(() => {
  const swiper = new Swiper(projectsSlider.value, {
    modules: [Navigation],
    slidesPerView: 2,
    spaceBetween: 24,
    // loop: true,
    navigation: {
      nextEl: btnRight.value,
      prevEl: btnLeft.value,
    },
  });
})

const cards = [
  {
    title: 'Clément Turpin will referee Napoli-Real Madrid',
    text:  'This will be the sixth time that the French referee has taken charge of a Champions League match for our team.',
    img: '/src/images/ref.png'
  },

  {
    title: 'Ancelotti: "Winning here shows that our defensive work was very good"',
    text:  '"Girona play good football but my team played a solid and convincing game," said the Real Madrid coach.',
    img: '/src/images/coach.png'
  },

  {
    title: 'Bellingham: "Whenever I put on this shirt I always try to do my best"',
    text:  '    "I\'ve been watching Modrić every day for three months. I just want to be creative," ' +
        'explained the Englishman about his assist.',
    img: '/src/images/bel.png'
  },
]

</script>

<style scoped lang="scss">
.news {
  flex-direction: row;
  margin-top: 10px;
  justify-content: space-between;
  width: 85%;
  margin-bottom: 10px;
  @media screen and (max-width: 400px) {
    .swiper-wrapper {
      * {
         * {
           width: 100%;
         }
      }
    }
  }
    img {
      width: 100%;
    }
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

.icon-arrow-left,.icon-arrow-right  {
  font-size: 32px;
  position: absolute;
  top: 78px;
  z-index: 1;
  transition: .2s;
  color: #449fdb;
  &:active{
    transform: scale(1.2);
  }
}
.icon-arrow-right{
  right: 5px;
}
.icon-arrow-left{
  left: 5px;
}

</style>