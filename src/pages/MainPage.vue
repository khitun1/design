<template>
  <div>
    <header>
      <StartNavbar v-if="showFirst" class="first"/>
      <VNavbar v-else/>
    </header>
    <main>
      <div class="empty"/>
      <AfterScrolling/>
    </main>
  </div>
</template>

<script setup lang="ts">
import AfterScrolling from "@/components/AfterScrolling.vue";
import {onBeforeUnmount, onMounted, ref} from "vue";
import StartNavbar from "@/components/StartNavbar.vue";
import VNavbar from "@/components/VNavbar.vue";

const showFirst = ref(true);

const onScroll = () => {
  showFirst.value = window.pageYOffset <= 650;
}

onMounted(() => {
  document.addEventListener('scroll', onScroll);
})


onBeforeUnmount(() => {
  document.removeEventListener('scroll', onScroll);
})

</script>

<style lang="scss">

  body {
    margin: 0;
    background-image: url('../images/Stadium.png');

  }


  .empty {
    background: none;
    height: 750px;
  }



</style>