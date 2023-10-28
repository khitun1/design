<template>
  <div class="band">
    <trophy-component :amount="amount[0]" :description="des[0]">
      <img src="../images/best.png"/>
    </trophy-component>

    <trophy-component :amount="amount[1]" :description="des[1]">
      <img src="../images/europeanCup.png"/>
    </trophy-component>

    <trophy-component :amount="amount[2]" :description="des[2]">
      <img src="../images/europeanSuperCup.png"/>
    </trophy-component>

    <trophy-component :amount="amount[3]" :description="des[3]">
      <img src="../images/uefa.png"/>
    </trophy-component>

    <trophy-component :amount="amount[4]" :description="des[4]">
      <img src="../images/laLiga.png"/>
    </trophy-component>
  </div>
</template>

<script setup lang="ts">

import TrophyComponent from "@/components/trophyComponent.vue";

const amount = ['', '14', '5', '2', '35'];

const des = ['THE BEST CLUB OF THE 20TH CENTURY FIFA TROPHY',
    'EUROPEAN CUPS',
    'EUROPEAN SUPER CUPS',
    'UEFA CUPS',
    'NATIONAL LEAGUES'];
</script>

<style scoped>

.band {
  display: flex;
}
</style>