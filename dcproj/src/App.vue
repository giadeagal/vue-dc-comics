<template>
  <div id="app">

    <header>
      <Header/>
    </header>

    <main>
      <Main/>
    </main>

    <!-- <footer>
      <Footer/>
    </footer> -->
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
// import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    // Footer
  }
}
</script>

<style lang="scss">
@import "style/commons.scss";
</style>
