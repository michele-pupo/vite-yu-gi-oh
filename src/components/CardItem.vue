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
    <img :src="cards.card_images[0].image_url" :alt="cards.name">
    <span>{{ cards.name }}</span>
    <strong>{{ cards.archetype }}</strong>
  </li>
</template>

<style lang="scss">
@use '../styles/_variables' as *;

   #single-card{
        text-align: center;
        background-color: $bg-color-card;
        display: flex;
        flex-flow: column;
        width: calc(100% / 5 - $card-gap / 5 * 4 );

        span{
            color: white;
            margin-top: 20px;
            font-size: 20px;
        }

        strong{
            margin: 20px 0px;
            font-size: 20px;
            font-weight: 400;
        }
   }
</style>