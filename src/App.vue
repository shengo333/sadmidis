<template>
    <div id="conteiner">
      <Header />
      <Main />
      <Footer />
    </div>
</template>

<script>

import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Footer,
    Header,
    Main
  }
}
</script>

<style scoped>
#app {
  font-family: Georgia, 'Times New Roman', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background: whitesmoke;
}
#conteiner{
  display: block;
  padding: 10px 0 20px 40px;
}
</style>
