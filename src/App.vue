<script>
  import axios from 'axios';
  import { store } from './store.js';
  import AppTitle from './components/AppTitle.vue';
  import AppContainer from './components/AppContainer.vue';
  import CardSearch from './components/CardSearch.vue';

  export default{

    components: {
      AppTitle,
      AppContainer,
      CardSearch
    },

    data() {
      return {
        store,
      }
    },

    created() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0').then(res => {
        // console.log(res.data.data)
        this.store.cards = res.data.data;
      })
    },

    methods: {
      searchCards() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
          .then(res => {
            // console.log(res.data)
            this.store.archetypes = res.data;
        });
      }
    }
  };
</script>

<template>

    <AppTitle></AppTitle>
    <CardSearch @search="searchCards()"></CardSearch>
    <AppContainer></AppContainer>

</template>

<style lang="scss">
  @use './styles/general.scss' as *;
</style>
