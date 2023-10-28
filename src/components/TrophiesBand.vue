<template>
  <div class="band">
    <TrophyComponent v-for="(trophy, index) in trophies" :key="index"
        :amount="trophy.amount" :description="trophy.description">
      <img :src="trophy.img" alt="trophy"/>
    </TrophyComponent>
  </div>
</template>

<script setup lang="ts">

import TrophyComponent from "@/components/TrophyComponent.vue";

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

<style scoped>

.band {
  display: flex;
}
</style>