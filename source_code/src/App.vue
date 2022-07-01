<template>
  <indexPage />
</template>

<script>
import indexPage from "./components/indexPage.vue";

export default {
  name: "App",
  components: {
    indexPage,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Arima:wght@100;200;600&display=swap");

body {
  height: 100vh;
  overflow-y: hidden;
  overflow-x: hidden;
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Inter", sans-serif;
  font-family: "Arima", cursive;
}
#app {
  height: 100%;
  width: 100%;
}
</style>
