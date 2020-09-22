<template>
  <div id="app">
    <Screen class="red" />
    <HorizontalSlide />
    <Screen class="blue" />
    <Gallery />
  </div>
</template>

<script>
import smoothscroll from "smoothscroll-polyfill";
smoothscroll.polyfill();

import Screen from "./components/Screen.vue";
import HorizontalSlide from "./components/HorizontalSlide.vue";
import Gallery from "./components/Gallery";

export default {
  name: "App",
  components: {
    Screen,
    HorizontalSlide,
    Gallery,
  },
  created: function() {
    console.log("here I am");
    document.getElementById("app").style.width = innerWidth;
    document.getElementById("app").style.height = innerHeight;
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

*::-webkit-scrollbar {
  width: 0.25em;
}

/* *::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
} */

*::-webkit-scrollbar-thumb {
  background-color: black;
  outline: 0px solid slategrey;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 100%;
  overflow: auto;
  scroll-snap-type: y proximity;
}
.red {
  background: red;
}
.blue {
  background: blue;
}
</style>
