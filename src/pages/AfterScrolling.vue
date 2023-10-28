<template>
  <div class="main">
    <h1 class="headlines">LATEST HEADLINES</h1>
    <CardNews/>
    <hr>
    <div class="games">
      <h1>MATCHES</h1>
      <h1>STANDING</h1>
    </div>
    <div class="gender">
      <h2>MEN</h2>
      <h2>WOMEN</h2>
      <h2>YOUTH</h2>
    </div>
    <GamesBand/>
    <hr>
    <h2>REAL MADRID TROPHIES</h2>
    <trophies-band/>
    <Footer/>
  </div>
</template>

<script setup lang="ts">

import GamesBand from "@/components/gamesBand.vue";
import CardNews from "@/components/cardNews.vue";
import TrophiesBand from "@/components/trophiesBand.vue";
import Footer from "@/components/footer.vue";

</script>

<style scoped lang="scss">


h1, h2 {
  color: #004996;
  font-family: Arial;
}


.main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  background-color: white;
}

.headlines {
  width: 80%;
}

.games{
  display: flex;
  flex-direction: row;
  width: 80%;
  h1:not(:first-child) {
    margin-left: 30px;
  }
  h1:first-child {
    text-decoration: underline;
  }
}

.gender {
  display: flex;
  flex-direction: row;
  width: 70%;
  h2:not(:first-child) {
    margin-left: 60px;
  }
  h2:first-child {
    text-decoration: underline;
  }
}


hr {
  color: #B3B3B3;
  background-color: #E0E0E0;
  height: 0;
  width: 100%;
}



</style>