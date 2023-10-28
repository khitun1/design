<template>
  <div class="news">
    <CardComponent v-for="(card, index) in cards" :key="index"
        :title="card.title"
        :text="card.text"
    >
      <img :src="card.img" alt="picture"/>
    </CardComponent>
  </div>
</template>

<script setup lang="ts">
import CardComponent from "@/components/CardComponent.vue";

const cards = [
  {
    title: 'Clément Turpin will referee Napoli-Real Madrid',
    text:  'This will be the sixth time that the French referee has taken charge of a Champions League match for our team.',
    img: '/src/images/ref.png'
  },

  {
    title: 'Ancelotti: "Winning here shows that our defensive work was very good"',
    text:  '"Girona play good football but my team played a solid and convincing game," said the Real Madrid coach.',
    img: '/src/images/coach.png'
  },

  {
    title: 'Bellingham: "Whenever I put on this shirt I always try to do my best"',
    text:  '    "I\'ve been watching Modrić every day for three months. I just want to be creative," ' +
        'explained the Englishman about his assist.',
    img: '/src/images/bel.png'
  },
]

</script>

<style scoped>
.news {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 85%;
}
</style>