<template>
  <div id="app">
    <Header />
    <router-view />
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "app",
  components: {
    Header
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
