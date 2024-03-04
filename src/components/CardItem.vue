<script>
    export default{
        name: 'CardItem',

        props: {
            cards: Object,
        },
    }
</script>

<template>
  <li id="single-card">
    {{ cards.name }}
    <img :src="cards.card_images[0].image_url" :alt="cards.name">
  </li>
</template>

<style lang="scss">
   #single-card{
        display: flex;
        flex-flow: column;
   }
</style>