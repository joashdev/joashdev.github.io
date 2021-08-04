<template>
  <section id="projects" class="section">
    <h1 class="is-family-monospace is-white is-size-1">#PROJECTS</h1>
    <div class="columns is-multiline is-flex is-justify-content-space-evenly">
      <Card
      v-for="(work, index) in works"
      v-bind:key="work.id"
      v-bind:index="index"
      v-bind:name="work.name"
      v-bind:desc="work.desc"
      v-bind:path="work.imgpath"
      v-bind:live="work.live"
      v-bind:repo="work.repo"
      >
      </Card>
    </div>
  </section>
</template>

<script>
import Card from './partials/Card';
const works = require('./data/data').projects;

export default {
  name: 'projects',
  components: {
    Card
  },
  data() {
    return { works };
  }
};
</script>

<style lang="scss" scoped>

</style>
