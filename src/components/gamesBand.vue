<template>
  <div class="band">
    <button class="prev">
      <img src="../images/prev.png">
    </button>
    <div class="matches">
      <GameComponent
          :score="scores[0]" :first-half="halfs[0]"
      >
        <img src="../images/girona.png"/>
        <img src="../images/real.png"/>
      </GameComponent>

      <GameComponent
          :score="scores[1]" :first-half="halfs[1]"
      >
        <img src="../images/napoli.png"/>
        <img src="../images/real.png"/>
      </GameComponent>

      <GameComponent
          :score="scores[2]" :first-half="halfs[2]"
      >
        <img src="../images/real.png"/>
        <img src="../images/osasuna.png"/>
      </GameComponent>

      <GameComponent class="current"
          :score="scores[3]" :first-half="halfs[3]" :cur="true"
      >
        <img src="../images/sevilla.png"/>
        <img src="../images/real.png"/>
      </GameComponent>

      <GameComponent
          :score="scores[4]" :first-half="halfs[4]"
      >
        <img src="../images/Braga.png"/>
        <img src="../images/real.png"/>
      </GameComponent>

      <GameComponent
          :score="scores[5]" :first-half="halfs[5]"
      >
        <img src="../images/barcelona.png"/>
        <img src="../images/real.png"/>
      </GameComponent>

      <GameComponent
          :score="scores[6]" :first-half="halfs[6]"
      >
        <img src="../images/real.png"/>
        <img src="../images/rayo.png"/>
      </GameComponent>
    </div>

    <button class="prev">
      <img src="../images/next.png">
    </button>
  </div>
</template>

<script setup lang="ts">
import GameComponent from "@/components/gameComponent.vue";

const scores = [
  '0 : 3', '2 : 3', '4 : 0', '07 D 08 H 30 M', 'Tue, 24/10', 'Sat, 28/10', 'Sun, 05/11',
]

const halfs = [
  '(0:2)', '(1:2)', '(1:0)', 'Sat, 21/10 ', '22:00 GMT+5', '17:35 GMT+5', '23:00 GMT+5',
]
</script>

<style scoped lang="scss">

.matches {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}

.band {
  display: flex;
  width: 85%;
}

.prev {
  background: none;
  border: none;
  cursor: pointer;
}

</style>