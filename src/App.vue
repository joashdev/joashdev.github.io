<template>
  <div class="" id="app">
    <Banner/>
    <Projects/>
    <About/>
    <Contact/>
  </div>
</template>

<script>
import Banner from './components/Banner';
import Projects from './components/Projects';
import About from './components/About';
import Contact from './components/Contact';

export default {
  name: 'app',
  components: {
    Banner, Projects, About, Contact
  }
}
</script>

<style lang="scss">
@import '/assets/scss/app.scss';
// @import '/assets/scss/debug.scss'; // for debugging
#app {
  max-width: 100% !important;
  overflow-x: hidden !important;
}

#app > section::before {
  display: block;
  content: '';
  margin-top: -50px;
  height: 50px;
  visibility: hidden;
  pointer-events: none;
}
</style>
