<template>
  <div>
    <start-nav-bar v-if="showFirst" class="first"/>
    <navBar v-else/>
    <div class="empty"/>
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
  console.log(window.pageYOffset)
  showFirst.value = window.pageYOffset <= 650;
})




</script>

<style lang="scss">

  body {
    background-image: url('../images/Stadium.png');
    background-repeat: no-repeat;
  }


  .empty {
    background: none;
    height: 720px;
  }



</style>