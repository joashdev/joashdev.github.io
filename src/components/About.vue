<template>
  <section id="about" class="section">
    <h1 class="is-family-monospace is-white is-size-1">#ABOUT</h1>
    <h1
      class="is-family-primary has-text-weight-bold is-white is-size-2 mx-3 pt-3">
      Education
    </h1>
    <div>
      <div class="columns is-multiline is-flex is-justify-content-center">
        <CompactCard
          v-for="(school, index) in educ"
          :key="index"
          :name="school.name"
          :desc="school.desc"
          :path="school.imgpath"
        />
      </div>
    </div>
    <h1
      class="is-family-primary has-text-weight-bold is-white is-size-2 mx-3 pt-3">
      Skills
    </h1>
    <div v-for="(category, index) in skills" :key="index">
      <h1 class="is-family-primary has-text-centered is-white is-size-3">
        {{ category.name }}
      </h1>
      <div class="columns is-multiline is-flex is-justify-content-center">
        <CompactCard
          v-for="(lang, ind) in category.items"
          :key="ind"
          :name="lang.name"
          :path="lang.imgpath"
          :size="'is-32x32'"
        />
      </div>
    </div>
    <h1
      class="is-family-primary has-text-weight-bold is-white is-size-2 mx-3 pt-3">
      Joash
    </h1>
    <div class="box has-box-shadow mx-3">
      <p class="subtitle">{{ joashname}}</p>
      <p class="subtitle has-text-centered is-italic">{{ joashdesc }}</p>
    </div>
  </section>
</template>

<script>
import CompactCard from './partials/CompactCard';

const skills = require('./data/data').skills;
const educ = require('./data/data').education;

export default {
  name: 'about',
  components: {
    CompactCard
  },
  data() {
    return {
      skills,
      educ,
      joashname: 'I was once inspired by a song that I heard on TV, and this time, allow me to share that song to you all:',
      joashdesc: 'Stori opmalay serchinpordaray Keepkeepsapodami, Soroweemasow Kosisisaron Rililabsmahkempani, Hismodanaman endisismordanlab Darisondadaskaywisbloo Kosemrolinin Kosamganagen Entuhemayjaskenbetru (Stori opmalay by Marian Rivera, 2018)'
    };
  }
};
</script>

<style lang="scss" scoped>
</style>
