<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from "./components/AppJumbo.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppJumbo,
   
  },
}

</script>


<template>

  <div>
    <AppHeader></AppHeader>
    <AppJumbo></AppJumbo>
    <AppMain></AppMain>
    <AppFooter></AppFooter>

  </div>
</template>


<style lang="scss">
</style>