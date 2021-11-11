<template>
  <main>
    <div class="containerMain">
      <h1> {{titleMain}} </h1>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
    titleMain: String,
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
    background: black;
    
    .containerMain{
      max-width: $container_width;
      padding: $padding-Y;
      margin: auto;

      h1{
        color: white;
        font-size: 30px;
      }
    }
  }
</style>