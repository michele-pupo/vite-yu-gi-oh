<script>
    import AppCards from './AppCards.vue';
    import { store } from '../store';

    export default{
        name: 'AppContainer',
        components: { AppCards },

        data() {
          return {
            store,
            isLoading: true,
          }
        },

        created() {
            // simuliamo un ritardo di caricamento
            setTimeout(() => {
                this.isLoading = false; 
            }, 1000); 
        }
    }
</script>

<template>
  <div id="container-orange">
    <div id="container-white">
        <div id="number-cards">
            {{ isLoading ? 'Loading...' : `Found ${store.cards.length} cards` }}
        </div>
        <AppCards v-if="!isLoading"></AppCards>
    </div>
  </div>
</template>

<style lang="scss">
@use '../styles/_variables' as *;

    #container-orange{
        background-color: $bg-color-card;
        padding-bottom: 100px;

        #container-white{
            background-color: #ffffff;
            width: calc(100vw - 320px);
            margin: 0 auto;
            padding: 50px;

            #number-cards{
                background-color: #212529;
                padding: 20px 0px 20px 15px;
                font-weight: bold;
                font-size: 25px;
            }
        }
    }
</style>
