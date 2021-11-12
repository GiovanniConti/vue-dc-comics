<template>
  <section class="cardsSection">
    <div class="cardsContainer">
      <ProductCard
      v-for="(card, i) in cardsList"
      :key="i"
      :img='card.thumb'
      :title='card.series'
      />
      <div class="containerBtn">
        <button class="btn_loadMore">LOAD MORE</button>
      </div>
      <div class="currentSeries">CURRENT SERIES</div>
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
  padding-bottom: 20px;

  .cardsContainer{
    width: $container_width;
    margin: auto;
    display: $display_flex;
    flex-wrap: wrap;
    gap: 40px 20px;
    position: relative;
    
    .containerBtn{
      width: 100%;
      text-align: center;

      .btn_loadMore{
        background: $color_primary;
        color: white;
        font-weight: bold;
        padding: 10px 40px;
        border: 0;
      }
    }

    .currentSeries{
      position: absolute;
      top: -40px;
      left: -25px;
      width: 250px;
      padding: 10px 16px;
      background-color: $color_primary;
      color: white;
      font-weight: bold;
      font-size: 20px;
      text-align: center;
      transform: translateY(-50%);
    }
  }

  

}

</style>