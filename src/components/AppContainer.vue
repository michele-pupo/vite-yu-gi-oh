<script>
    import AppCards from './AppCards.vue';
    import { store } from '../store';

    export default{
        name: 'AppContainer',
        components: { AppCards },

        data() {
          return {
            store,
          }
        },
    }
</script>

<template>
  <div id="container-orange">
    <div id="choice">
        <select id="choice-type">
            <option value="easy">Alien</option>
            <option value="medium">Infermoble Arms</option>
            <option value="hard">Noble Knight</option>
        </select>
    </div>
    <div id="container-white">
        <div id="number-cards">
            Found {{ store.cards.length }} cards
        </div>
        <AppCards></AppCards>
    </div>
  </div>
</template>

<style lang="scss">
    #container-orange{
        background-color: #d48f38;

        #choice{
            width: calc(100vw - 320px);
            margin: 0 auto;
            padding: 35px 0px 35px 18px;

            #choice-type{
                background-color: white;
                color: black;
                font-size: 18px;
                padding: 10px 70px 10px 10px;
                border-color: transparent;
                border-radius: 5px;
                cursor: pointer;
            }
        }

        #container-white{
            background-color: #ffffff;
            width: calc(100vw - 320px);
            margin: 0 auto;
            padding: 50px;

            #number-cards{
                background-color: #212529;
                padding: 20px 0px 20px 15px;
                font-weight: bold;
            }
        }
    }
</style>
