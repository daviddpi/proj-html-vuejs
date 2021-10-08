<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/color.scss';

::-webkit-scrollbar {
  width: 12px;
}

::-webkit-scrollbar-track{
  background-color: #eef7fb;
  border-radius: 25px;
  margin-block: -0.2rem;
}

::-webkit-scrollbar-thumb{
  background-color: #bbbbbb;
  border-radius: 25px;
}

</style>
