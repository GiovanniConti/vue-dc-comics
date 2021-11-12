<template>
  <section class="cardsSection">
    <div class="cardsContainer">
      CARDS
    </div>

  </section>
</template>

<script>
export default {
  name: "CardsContainer",
  props: { },
  components: {

  },
  data() {
    return {

    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.cardsSection{
  background: rgb(28, 28, 28);
  min-height: 300px;
  padding: $padding-Y;

  
  .cardsContainer{
    width: $container_width;
    
    margin: auto;
    background-color: slategrey;
    min-height: 100px;
  }
}

</style>