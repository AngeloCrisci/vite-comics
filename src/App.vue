<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppHero from './components/AppHero.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppHero,
  }
}


</script>

<template>
  <AppHeader />
  <AppMain />
  <AppHero />
  <AppFooter />
</template>

<style lang="scss">
@use '../node_modules/bootstrap/scss/bootstrap.scss' as *;
@use 'style.scss' as *;
</style>
