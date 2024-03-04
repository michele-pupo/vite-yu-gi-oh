<script>
  import axios from 'axios';
  import { store } from './store.js';
  import AppTitle from './components/AppTitle.vue';
  import AppContainer from './components/AppContainer.vue';

  export default{

    components: {
      AppTitle,
      AppContainer
    },

    data() {
      return {
        store,
        isLoading: true
      }
    },

    created() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0').then(res => {
        // console.log(res.data.data)
        this.store.cards = res.data.data;
      })
    },

    methods: {
    fetchData() {
      // Simuliamo una chiamata API che ritorna dei risultati dopo un certo tempo
      setTimeout(() => {
        // Qui dovresti fare la tua effettiva chiamata API
        // Quando i risultati sono pronti, imposta isLoading su false
        // Esegui questa operazione all'interno del then() o della callback di successo della tua chiamata API
        this.isLoading = false;
      }, 2000); // Simuliamo un ritardo di 2 secondi
    }
  }
  }
</script>

<template>

    <AppTitle></AppTitle>
    <AppContainer></AppContainer>

</template>

<style lang="scss">
  @use './styles/general.scss' as *;
</style>
