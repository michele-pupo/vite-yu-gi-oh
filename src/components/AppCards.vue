<script>
  import { store } from '../store';
  import CardItem from './CardItem.vue';

    export default{
        name: 'AppCards',

        components:{
          CardItem
        },

        data() {
          return {
            store,
          }
        },
    }
</script>
  
<template>
  <div id="cards">
    <ul>
      <CardItem 
        v-for="currentCard in store.cards"
        :cards="currentCard"
      ></CardItem>
    </ul>
  </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

   #cards{
    color: black;

    ul{
      list-style-type: none;
      display: flex;
      flex-flow: row wrap;
      gap: $card-gap;
    }
   }
</style>