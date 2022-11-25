<script>
import MagazineSection from './MagazineSection.vue';

export default {
  name: "AppMain",
  components: {
    MagazineSection
  }
};
</script>

<template>
  <main>
    <section class="jumbotron"></section>
    <MagazineSection/>
  </main>
</template>

<style lang="scss" scoped>
main {
  background-color: var(--bg-main-color);
  & .jumbotron {
    background-image: url("../assets/jumbotron.jpg");
    background-size: cover;
    height: 555px;
  }
}
</style>
