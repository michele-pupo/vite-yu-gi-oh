<script>
  export default{
        name: 'CardSearch',
    }

</script>
  
<template>
  <div id="choice">
    <select id="choice-type">
        <option>Alien</option>
        <option>Infermoble Arms</option>
        <option>Noble Knight</option>
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