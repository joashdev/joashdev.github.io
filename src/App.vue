<template>
  <div class="" id="app">
    <Banner/>
    <Projects/>
    <!-- <button class="button is-family-primary" @click="changeText">Change Text</button>
    <Sample sampleProp="Some • text here"/>
    <Sample :sampleProp="secondaryMessage"/> -->
    <About/>
    <Contact/>
  </div>
</template>

<script>
import Sample from './components/Sample';
import Banner from './components/Banner';
import Projects from './components/Projects';
import About from './components/About';
import Contact from './components/Contact';

export default {
  name: 'app',
  components: {
    Sample, Banner, Projects, About, Contact
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      secondaryMessage: ''
    }
  },
  methods: {
    changeText() {
      this.secondaryMessage = 'Ayoooo noice';
    }
  }
}
</script>

<style lang="scss">
@import '/assets/scss/app.scss';
// @import '/assets/scss/debug.scss';  
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
