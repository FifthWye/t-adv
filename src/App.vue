<template>
  <div id="app">
    <Header />
    <Body />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Body from "./components/Body.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Body,
    Footer
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Nanum+Gothic&display=swap");

#app {
  font-family: "Nanum Gothic", Arial, sans-serif;
  color: #2c3e50;
  background: white;
}

.row {
  width: 100%;
}
</style>
