<template>
  <div class="card">
    <slot>

    </slot>
    <h1>{{title}}</h1>
    <p>{{text}}</p>
  </div>
</template>

<script setup lang="ts">

const {title, text} = defineProps({
  title: String,
  text: String,
})
</script>

<style scoped lang="scss">

h1 {
  color: #DFB51E;
  font-size: 20px;
  font-weight: bolder;
}

p {
  color: #818181;
  font-size: 20px;
}

.card {
    background: #ffffff;
    width: 431px;
    h1, p {
      margin-left: 3px;
    }
}
</style>