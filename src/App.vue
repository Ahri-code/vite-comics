<script>
import HeaderApp from './components/HeaderApp.vue'
import MainApp from './components/MainApp.vue'
import FooterApp from './components/FooterApp.vue'

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  }
}
</script>

<template>
  <header>
    <HeaderApp />
  </header>
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
header {
  background-color: #fff;
  width: 100%;
  display: flex;
  justify-content: center;
}
</style>
