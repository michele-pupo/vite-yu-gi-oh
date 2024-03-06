<script>
  import { store } from '../store';  

  export default{
        name: 'CardSearch',

        data() {
          return {
            store,
          }
        },
    }

</script>
  
<template>
  <div id="choice">
    <select 
        id="choice-type"  
        name="archetype" 
        v-model="store.searchCards" 
        @change="$emit('search')">
        <option selected value="">Filtra archetype...</option>
        <option v-for="archetype in store.archetypes" :value="archetype.archetype_name ">{{ archetype.archetype_name }}</option>
    </select>
    </div>
</template>

<style lang="scss">
@use '../styles/_variables' as *;

    #choice{
        background-color: $bg-color-card;
        margin: 0 auto;
        padding: 35px 0px 35px 170px;

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
</style>