<template>
  <section class="cardsSection">
    <div class="cardsContainer">
      <ProductCard
      v-for="(card, i) in cardsList"
      :key="i"
      :img='card.thumb'
      :title='card.series'
      />
    </div>

  </section>
</template>

<script>
import CardsData from '../database/dc-comics.json'
import ProductCard from './ProductCard.vue'

export default {
  name: "CardsContainer",
  props: {

  },
  components: {
    ProductCard,
  },
  data() {
    return {
      cardsList: CardsData,
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
    display: $display_flex;
    flex-wrap: wrap;
    gap: 40px 20px;
    
  }
}

</style>