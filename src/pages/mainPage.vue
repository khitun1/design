<template>
  <div>
    <start-nav-bar v-if="showFirst" class="first"/>
    <div class="empty"/>
    <navBar v-if="!showFirst"/>
    <after-scrolling />
  </div>
</template>

<script setup lang="ts">

import StartNavBar from "@/components/startNavBar.vue";
import AfterScrolling from "@/pages/AfterScrolling.vue";
import NavBar from "@/components/navBar.vue";
import {ref} from "vue";

const showFirst = ref(true);


document.addEventListener('scroll', e => {
  showFirst.value = window.pageYOffset <= 650;
})




</script>

<style lang="scss">

  body {
    background-image: url('../images/Stadium.png');

  }


  .empty {
    background: none;
    height: 720px;
  }



</style>