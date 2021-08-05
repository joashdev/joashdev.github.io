<template>
  <section class="banner is-paddingless-horizontal" id="home">
    <Navbar />
    <Hero />
  </section>
</template>

<script>
import Navbar from './partials/Navbar';
import Hero from './partials/Hero';

export default {
  name: 'banner',
  components: {
    Navbar,
    Hero
  }
};
</script>

<style lang="scss"scoped>
.banner /deep/ *  {
  color: #fff
  }
</style>
