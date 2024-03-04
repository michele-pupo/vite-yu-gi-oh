<script>
  import AppTitle from './components/AppTitle.vue';
  import AppContainer from './components/AppContainer.vue';

  export default{

    components: {
      AppTitle,
      AppContainer
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
