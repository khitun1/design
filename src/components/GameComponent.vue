<template>
  <div class="main">
    <div class="logo">
      <slot>
      </slot>
    </div>
    <div class="score"  v-bind:style="{color: cur ? '#FF111F' : '#004996'}">
      {{score}}
    </div>
    <div class="firstHalf">
      {{firstHalf}}
    </div>
  </div>
</template>

<script setup>

const {score, firstHalf, cur} = defineProps({
  score: String,
  firstHalf: String,
  cur: Boolean
})

</script>

<style scoped lang="scss">
  .score {
    display: flex;
    justify-content: center;
    font-weight: bold;
    font-size: 24px;
    font-family: Arial;

    @media screen and (max-width: 400px) {
      font-size: 12px;
    }
  }

  .firstHalf {
    display: flex;
    justify-content: center;
    font-size: 24px;
    color: #B3B3B3;
    font-family: Arial;
    @media screen and (max-width: 400px) {
      font-size: 12px;
    }
  }

  .logo {
    display: flex;
    justify-content: center;
  }

  .main {
    @media screen and (max-width: 400px) {
      height: 70px;
    }

  }
</style>