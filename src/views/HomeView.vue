<template>
  <v-app>
    <Navbar class="index" />
    <Dashboard />
    <Footer />
  </v-app>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Dashboard from "../components/Dashboard.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",

  components: {
    Navbar,
    Dashboard,
    Footer,
  },
};
</script>

<style scoped>
.index {
  z-index: 9999;
}
</style>