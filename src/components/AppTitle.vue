<script>
    export default{
        name: 'AppTitle',
    }
</script>

<template>
  <div id="title">
    <div id="logo">
        <img src="../../public/img/favicon.jpg" alt="logo">
    </div>
    <h1>Yu-gi-oh Api</h1>
  </div>
</template>

<style lang="scss">
    #title{
        background-color: white;
        color: black;
        display: flex;
        align-items: baseline;
        height: 100px;
        padding-left: 40px;
        padding-top: 10px;
        gap: 30px;

        h1{
            text-transform: uppercase;
            font-size: 50px;
        }

        #logo{
            height: 30px;

            img{
                height: 100%;
            }
        }
    }

</style>
