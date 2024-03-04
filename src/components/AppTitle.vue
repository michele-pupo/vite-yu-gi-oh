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
        display: flex;
        align-items: baseline;
        height: 100px;
        padding-top: 10px;
        gap: 30px;

        h1{
            color: black;
            font-size: 50px;
            font-weight: 400;
            text-transform: uppercase;
        }

        #logo{
            height: 30px;
            padding-left: 40px;

            img{
                height: 100%;
            }
        }
    }
</style>
