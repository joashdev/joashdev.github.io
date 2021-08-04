<template>
  <section class="hero is-fullheight">
    <div class="hero-body">
      <div class="">
        <p class="title">Kent Joash A. Zamudio</p>
        <p class="subtitle">Software Developer at Itemhound Corp</p>
        <span class="icon-text is-flex is-justify-content-space-around ">
          <a
            href="#contact"
            class="button m-1 is-danger is-outlined is-rounded"
          >
            <span class="icon is-small">
              <i class="fas fa-comment"></i>
            </span>
            <span>Let's talk</span>
          </a>
          <a
            class="button m-1 is-danger is-outlined is-rounded"
            @click="downloadResume"
          >
            <span class="icon is-small">
              <i class="fas fa-download"></i>
            </span>
            <span>My Resume</span>
          </a>

        </span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'hero',
  methods: {
    downloadResume: function() {
      window.open('/src/assets/doc/Resume-Zamudio-Kent-Joash.pdf');
    }
  }
};
</script>

<style lang="scss">
.hero-body {
  background: black url(/src/assets/img/hero-1.jpg) center / cover;
  padding-left: 10rem;
}
@media screen and (max-width: 1024px) {
  .hero-body {
    background: black url(/src/assets/img/hero-2.jpg) right / cover;
    text-align: center;
  }
}
@media screen and (max-width: 768px) {
  .hero-body {
    text-align: center;
    background: black url(/src/assets/img/hero-3.jpg) right / cover;
    padding-left: 2rem;
  }
}
</style>
