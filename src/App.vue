<template>
  <div id="app">
    <Welcome />
    <Screen class="dots" />
    <HorizontalSlide />
    <Screen class="hex" />
    <Gallery @showItem="showItem()" />
    <Footer />
    <Overlay :show="showOverlay" />
    <Drama :show="showDrama" />
  </div>
</template>

<script>
import smoothscroll from "smoothscroll-polyfill";
smoothscroll.polyfill();

import Screen from "./components/Screen";
import HorizontalSlide from "./components/HorizontalSlide";
import Gallery from "./components/Gallery";
import Overlay from "./components/Overlay";
import Welcome from "./components/Welcome";
import Footer from "./components/Footer";
import Drama from "./components/Drama";

export default {
  name: "App",
  components: {
    Screen,
    HorizontalSlide,
    Gallery,
    Overlay,
    Welcome,
    Footer,
    Drama,
  },
  data: function() {
    return {
      showOverlay: false,
      showDrama: true,
    };
  },
  methods: {
    showItem: function() {
      this.showOverlay = false;
      console.log("toggle");
      this.showOverlay = true;
    },
    goto: function(anchorname) {
      document
        .getElementById(anchorname)
        .scrollIntoView({ behavior: "smooth" });
    },
    setsize: function() {
      var newheight = window.innerHeight + "px";
      var newwidth = window.innerWidth + "px";
      document.body.style.setProperty("height", newheight);
      document.body.style.setProperty("width", newwidth);
    },
  },
  created: function() {
    this.setsize();
    window.addEventListener("resize", this.setsize);
  },
  destroyed: function() {
    window.removeEventListener("resize", this.setsize);
  },
  mounted: function() {
    const history = document.getElementsByClassName("slideholder")[0];
    history.scrollLeft = history.scrollWidth - history.offsetWidth;
  },
};
</script>

<style>
html {
  scroll-behavior: smooth;
}

body {
  margin: 0px;
  background: black;
  box-sizing: border-box;
  color: white;
  height: 100vh;
  width: 100vw;
  font-size: 2em;
}

*::-webkit-scrollbar {
  width: 0.25em;
  height: 0.25em;
}

/* *::-webkit-scrollbar-track {
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
} */

*::-webkit-scrollbar-thumb {
  background-color: black;
  outline: 0px solid slategrey;
}

#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 100%;
  overflow: auto;
  scroll-snap-type: y proximity;
}
.red {
  background-color: red;
}
.blue {
  background-color: blue;
}
.dots {
  background-image: url("assets/dots.svg");
}

.hex {
  background-image: url("assets/hexadots.svg");
}
</style>
