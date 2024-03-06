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

      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0')
        .then(res => {
          console.log('carte', res.data.data)
          this.store.cards = res.data.data;
        });

      // chiamata api per popolare la select di scelta archetipo
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
        .then(res => {
          console.log('archetipi', res.data)
          this.store.archetypes = res.data;
        })

      },

      methods: {

        searchCards() {
          // console.log('Richiesta di filtro')
          axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0&archetype=' + this.store.searchCards) 
            .then(res => {
              console.log('Numero di carte', res.data.meta.total_rows)
              this.store.numberOfCards = res.data.meta.total_rows;
              this.store.cards = res.data.data;
          });
        },

        },
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
