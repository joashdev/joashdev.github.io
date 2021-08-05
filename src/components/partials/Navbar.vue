<template>
  <section>
    <nav class="navbar is-transparent is-fixed-top">
      <!-- nav bar left side -->
      <div class="navbar-brand ">
        <a href="#home" class="navbar-item is-family-secondary is-size-4">
          <img
            src="/src/assets/img/banner-logo.png"
            alt="kent joash zamudio logo"
          />
          kent joash
        </a>
        <span
          data-target="nav-links"
          @click="isActive = !isActive"
          :class="[isActive ? activeClass : '', 'navbar-burger']"
        >
          <span></span>
          <span></span>
          <span></span>
        </span>
      </div>
      <div
        id="nav-links"
        v-bind:class="[
          isActive ? activeClass : '',
          'navbar-menu',
          'is-transparent'
        ]"
      >
        <div class="navbar-end is-pulled-right pr-6">
          <a href="#projects" class="navbar-item hover-under" @click="isActive = !isActive">Projects</a>
          <a href="#about" class="navbar-item hover-under" @click="isActive = !isActive">About</a>
          <a href="#contact" class="navbar-item hover-under" @click="isActive = !isActive">Contact</a>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  name: 'navbar',
  data: function () {
    return {
      isActive: false,
      activeClass: 'is-active'
    };
  }
};
</script>

<style lang="scss">
.navbar,
.navbar-menu {
  &.is-transparent {
    background-color: rgba(33, 33, 33, 0.4);
    background-image: none;
  }
}
.navbar-brand a:hover {
  color: white;
}
.navbar-menu a:hover {
  color: red;
  font-weight: bold;
  background-color: transparent;
}
</style>
