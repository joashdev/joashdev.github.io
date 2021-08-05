<template>
<div class="column is-2">
    <div class="level mb-0">
        <div class="level-item">
            <figure :class="['image', size]">
                <img :src="path" alt="">
            </figure>
        </div>
    </div>
    <h5 class="title is-size-5 my-1">{{name}}</h5>
    <p v-if="desc && desc.length" class="desc">{{desc}}</p>
</div>
</template>

<script>
export default {
  name: 'compactcard',
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
    size: {
      type: String,
      default: 'is-128x128'
    }
  }
};
</script>
<style lang="scss" scoped>
.column {
    border: 1px lightgray solid;
  margin: 10px;
  text-align: center;
  -webkit-box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
  -moz-box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
  box-shadow: -7px 11px 25px -9px rgba(0, 0, 0, 1);
}
@media screen and (max-width: 768px) {
  .is-size-5{
    font-size: .75rem !important;
  }
  .desc{
    font-size: .75rem !important;
  }
}
@media screen and (max-width: 769px) {
  .is-size-5{
    font-size: .75rem !important;
  }
  .desc{
    font-size: .75rem !important;
  }
}
</style>
