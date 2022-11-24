<script setup>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppDcBar from './components/AppDcBar.vue';
  import AppFooter from './components/AppFooter.vue'
</script>

<template>
  <!-- Header --><AppHeader/><!-- /Header -->
  <!-- Main --><AppMain/><!-- /Main -->

  <footer>
    <!-- Pre-footer -->
    <AppDcBar/>

    <!-- Footer Main & Bottom -->
    <AppFooter/>
  </footer>
</template>

<style lang="scss">
  @import './style/global.scss'
</style>
