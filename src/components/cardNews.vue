<template>
  <div class="news">
    <CardComponent
        :title="titles[0]"
        :text="texts[0]"
    >
      <img src="../images/ref.png"/>
    </CardComponent>
    <CardComponent
        :title="titles[1]"
        :text="texts[1]"
    >
      <img src="../images/coach.png"/>
    </CardComponent>
    <CardComponent
        :title="titles[2]"
        :text="texts[2]"
    >
      <img src="../images/bel.png"/>
    </CardComponent>
  </div>
</template>

<script setup lang="ts">
import CardComponent from "@/components/cardComponent.vue";

const titles = ['Clément Turpin will referee Napoli-Real Madrid',
  'Ancelotti: "Winning here shows that our defensive work was very good"',
  'Bellingham: "Whenever I put on this shirt I always try to do my best"'];

const texts = [
  '    This will be the sixth time that the French referee has taken charge of a Champions League match for our team.',
  '    "Girona play good football but my team played a solid and convincing game," said the Real Madrid coach.',
  '    "I\'ve been watching Modrić every day for three months. I just want to be creative," ' +
  'explained the Englishman about his assist.'];
</script>

<style scoped>
.news {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 85%;
}
</style>