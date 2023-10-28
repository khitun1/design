<template>
  <div class="band">
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
    <button class="prev">
      <img src="../images/next.png" alt="next button">
    </button>
  </div>
</template>

<script setup lang="ts">
import GameComponent from "@/components/GameComponent.vue";

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
    score: '07 D 08 H 30 M',
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