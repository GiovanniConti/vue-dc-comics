<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/dc-logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header></Header>
    <Main titleMain='--> Content goes here <--'></Main>
    <SectionBlue></SectionBlue>
    <Footer></Footer>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import SectionBlue from './components/SectionBlue.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Header,
    Main,
    SectionBlue,
    Footer,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
