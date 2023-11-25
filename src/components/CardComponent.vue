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
  font-weight: bolder;
  font-family: Arial;
}

p {
  color: #818181;
  font-family: Arial;
  text-indent: 30px;
}

.card {
    background: #ffffff;

    width: 34%;
    h1, p {
      margin-left: 3px;
      font-size: 20px;
    }

  @media screen and (max-width: 400px) {
    h1{
      font-size: 14px;
    }
    p {
      display: none;
    }
  }
}

</style>