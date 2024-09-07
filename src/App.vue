<script>
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<template>
  <div class="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>
