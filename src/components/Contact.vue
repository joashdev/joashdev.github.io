<template>
  <section id="contact" class="section pt-5 has-background-grey-dark">
    <h1 class="is-family-monospace has-text-white is-size-1">#CONTACT</h1>
    <div class="my-5 mt-5 mx-5 is-flex is-justify-content-space-evenly">
      <form action="" method="post" class="" >
        <div class="field">
          <label
            for="name"
            class="label is-size-4 has-text-white"
          >Get in touch</label>
          <div class="control has-icons-left">
            <input
              type="text"
              name="name"
              id="name"
              class="input is-rounded is-info"
              placeholder="Name"
            />
            <span class="icon is-left">
              <i class="fa fa-user"></i>
            </span>
          </div>
        </div>
        <div class="field">
          <!-- <label
            for="email"
            class="label is-size-4 has-text-weight-light"
          ></label> -->
          <div class="control has-icons-left">
            <input
              type="email"
              name="email"
              id="email"
              class="input is-rounded is-info"
              placeholder="Email"
            />
            <span class="icon is-left">
              <i class="fa fa-envelope"></i>
            </span>
          </div>
        </div>
        <div class="field is-rounded">
          <!-- <label
            for="message"
            class="label is-size-4 has-text-weight-light"
          ></label> -->
          <textarea
            name="message"
            id="message"
            rows="5"
            class="textarea is-medium is-info"
            placeholder="Message"
          ></textarea>
        </div>
        <button type="submit" class="button is-info is-rounded is-fullwidth is-size-5">
          Submit
        </button>
      </form>

    </div>
  </section>
</template>

<script>
export default {
  name: 'contact'
};
</script>

<style lang="scss" scoped>
// #contact {
//   // background: black url(/src/assets/img/hero-bottom.jpg) top / cover;
//   // height: 300px;
// }
.textarea {
  border-radius: 25px;
}
</style>
