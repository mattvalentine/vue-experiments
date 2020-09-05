<template>
  <div id="app">
    <Screen />
  </div>
</template>

<script>
import Screen from "./components/Screen.vue";
export default {
  name: "App",
  components: {
    Screen,
  },
};
</script>

<style>
body {
  margin: 0px;
  background: black;
  box-sizing: border-box;
  color: white;
  height: 100vh;
  width: 100vw;
  /* display: flex; */
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 100%;
}
</style>
