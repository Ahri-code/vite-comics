<script>
import HeaderApp from './components/HeaderApp.vue'
import MainApp from './components/MainApp.vue'
import FooterApp from './components/FooterApp.vue'
import data from './assets/dc-comics.json';

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  },
  data() {
    return {
      myData: data
    }
  }
}
</script>

<template>
  <header>
    <HeaderApp />
  </header>
  <main>
    <MainApp v-for="i in data" :link="data[i].thumb" :cost="data[i].price" :series="data[i].series"
      :type="data[i].type" />
  </main>
  <footer>
    <FooterApp />
  </footer>
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
header {
  background-color: #fff;
  width: 100%;
  display: flex;
  justify-content: center;
}

main {
  width: 100%;
  background: #1c1c1c;
  color: white;
  display: flex;
  justify-content: center;
}

footer {
  width: 100%;
  color: white;
}
</style>
