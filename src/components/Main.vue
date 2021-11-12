<template>
  <main>
    <div class="containerHero">
      <img src="@/assets/jumbotron.jpg" alt="">
    </div>
    <CardsContainer/>
  </main>
</template>

<script>

import CardsContainer from './CardsContainer.vue'

export default {
  name: 'Main',
  props: {
    titleMain: String,
  },
  components: {
    CardsContainer,
  },
  data() {
    return {
      
    };
  },
}
</script>

<style lang="scss">
@import "../styles/variables.scss";

  main{
    
    .containerHero{
      max-height: 400px;
      overflow: hidden;
    }


    
  }
</style>