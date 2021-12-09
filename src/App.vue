<template>
  <div id="app">
    <Header />

    <Jumbo />

    <Main />

    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbo from './components/Jumbo.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Jumbo,
  }
}
</script>

<style lang="scss">

</style>
