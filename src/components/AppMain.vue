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
    <section class="jumbotron">
      <img src="../assets/jumbotron.jpg" alt="">
    </section>
    <MagazineSection/>
  </main>
</template>

<style lang="scss" scoped>
main {
  background-color: var(--bg-main-color);
  & .jumbotron img{
    width: 100%;
    max-height: 400px;
    object-fit: cover;
    object-position: top;
  }
}
</style>
