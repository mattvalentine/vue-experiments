<template>
  <div id="app">
    <Welcome />
    <Screen class="dots" />
    <HorizontalSlide />
    <Screen class="hex" />
    <Transition start="red" end="blue" />
    <Gallery @showItem="showItem()" />
    <Footer />
    <Overlay :show="showOverlay" />
    <Drama :show="showDrama" />
    <div class="testmenu">X</div>
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
import Transition from "./components/Transition";

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
    Transition,
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
      const appElement = document.getElementById("app");
      const newHeight = window.innerHeight + "px";
      const newWidth = window.innerWidth + "px";
      document.body.style.setProperty("height", newHeight);
      document.body.style.setProperty("width", newWidth);
      appElement.style.setProperty("height", newHeight);
      appElement.style.setProperty("width", newWidth);
    },
  },
  created: function() {
    this.setsize();
    window.addEventListener("resize", this.setsize);
    var lockFunction = window.screen.orientation.lock;
    if (lockFunction.call(window.screen.orientation, "landscape")) {
      console.log("Orientation locked");
    } else {
      console.error("There was a problem in locking the orientation");
    }
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
  font-size: 1.25em;
  position: absolute;
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

.dots {
  background-image: url("assets/dots.svg");
}

.hex {
  background-image: url("assets/hexadots.svg");
}

.testmenu {
  position: absolute;
  top: 10px;
  left: 10px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
  border-radius: 100%;
  width: 40px;
  height: 40px;
  color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: white;
  opacity: 50%;
}
</style>
