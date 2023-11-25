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
    <h1>REAL MADRID TROPHIES</h1>
    <TrophiesBand/>
    <VFooter/>
  </div>
</template>

<script setup lang="ts">

import GamesBand from "@/components/GamesBand.vue";
import CardNews from "@/components/CardNews.vue";
import TrophiesBand from "@/components/TrophiesBand.vue";
import VFooter from "@/components/VFooter.vue";

</script>

<style scoped lang="scss">


h1, h2 {
  color: #004996;
  font-family: Arial;
}

h1 {
  @media screen and (max-width: 400px) {
    font-size: 20px ;
  }
}

h2 {
  @media screen and (max-width: 400px) {
    font-size: 14px ;
  }
}


.main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  background-color: white;
  border-radius: 5px;
  margin-top: 20px;
}

.headlines {
  width: 80%;
}

.games{
  display: flex;
  flex-direction: row;
  width: 80%;
  h1 {
    cursor: pointer;
  }
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
  h2 {
    cursor: pointer;
  }
  h2:not(:first-child) {
    margin-left: 60px;
  }
  h2:first-child {
    text-decoration: underline;
  }

  @media screen and (max-width: 400px) {
    flex-direction: column;
    h2:not(:first-child) {
      margin-left: 0;
      margin-top: 10px;
    }
    margin-bottom: 20px;

  }
}


hr {
  color: #B3B3B3;
  background-color: #E0E0E0;
  height: 0;
  width: 98%;
}



</style>