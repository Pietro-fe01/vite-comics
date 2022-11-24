<script setup>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppDcBar from './components/AppDcBar.vue';
</script>

<template>
  <!-- Header --><AppHeader/><!-- /Header -->
  <!-- Main --><AppMain/><!-- /Main -->
  
  <!-- Footer -->
  <footer>
    <AppDcBar/>
  </footer>
  <!-- /Footer -->
</template>

<style lang="scss">
  @import './style/global.scss'
</style>
