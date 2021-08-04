<template>
  <div class="card column is-one-quarter mx-1 my-2">
    <header class="card-header">
      <p
        class="
          card-header-title
          is-centered
          has-text-grey has-weight-bold
          is-size-5
        "
      >
        {{ name }}
      </p>
    </header>

    <div class="card-image">
      <figure class="image is-fullwidth">
        <img :src="path" alt="Placeholder image" />
      </figure>
    </div>
    <div class="card-content">
      <div class="content">
        <p class="is-centered has-text-info">{{ desc }}</p>
      </div>
    </div>
    <footer class="card-footer">
      <a
        v-if="live && live.length"
        :href="live"
        target="_blank"
        class="card-footer-item has-text-danger hover-under"
        title="View Deployed App"
        >Live demo</a
      >
      <a
        v-else
        class="card-footer-item has-text-grey-light is-disabled"
        title="No Demo Available"
        >Live demo</a
      >
      <a
        :href="repo"
        target="_blank"
        class="card-footer-item has-text-danger hover-under"
        title="View App Repository"
        >View code</a
      >
    </footer>
  </div>
</template>

<script>
export default {
  name: 'card',
  props: {
    name: {
      type: String
    },
    desc: {
      type: String
    },
    path: {
      type: String
    },
    live: {
      type: String
    },
    repo: {
      type: String
    }
  }
};
</script>
<style lang="scss" scoped>
.column {
  margin: 10px;
  text-align: center;
  -webkit-box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
  -moz-box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
  box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
}

a.is-disabled {
  cursor: not-allowed;
}
</style>
