<template>
  <div class="card">
    <div class="card_containerImg">
      <img :src="img" :alt="title" class="card_containerImg_img">
    </div>

    <h4 class="card_title">{{ title }}</h4>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    img: {
      type: String,
      // default: "",      //insert default img
    },
    title: {
      type: String,
      // required: true,
    },
  },
  data() {
    return {

    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.card{
  width: calc((100% - 100px) / 6);

  .card_containerImg{
    width: 100%;
    height: 183px;
    overflow: hidden;
  }

  .card_title{
    color: white;
    font-weight: bold;
    padding-top: 12px;
  }
}

</style>