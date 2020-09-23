<template>
  <div class="overlay" v-show="show" @click="unshow">
    <div class="centerStart" id="center"></div>
    <div class="dark ftbstart" id="fader1"></div>
    <div class="dark ftbstart" id="fader2"></div>
    <div class="dark flrstart" id="fader3"></div>
    <div class="dark flrstart" id="fader4"></div>
  </div>
</template>

<script>
export default {
  name: "Drama",
  props: ["show"],
  methods: {
    unshow: function() {
      this.show = false;
    },
    grow: function() {
      console.log("grow");

      const centerElement = document.getElementById("center");
      const fader1Element = document.getElementById("fader1");
      const fader2Element = document.getElementById("fader2");
      const fader3Element = document.getElementById("fader3");
      const fader4Element = document.getElementById("fader4");

      centerElement.classList.add("centerEnd");
      fader1Element.classList.add("ftbend");
      fader2Element.classList.add("ftbend");
      fader3Element.classList.add("flrend");
      fader4Element.classList.add("flrend");

      centerElement.classList.remove("centerStart");
      fader1Element.classList.remove("ftbstart");
      fader2Element.classList.remove("ftbstart");
      fader3Element.classList.remove("flrstart");
      fader4Element.classList.remove("flrstart");

      setTimeout(this.unshow, 3000);
    },
  },
  mounted: function() {
    this.$nextTick(this.grow);
  },
};
</script>

<style>
.overlay {
  z-index: 200;
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  cursor: pointer;
}

#fader1 {
  width: 100%;
  position: absolute;
  top: 0%;
}
#fader2 {
  width: 100%;
  position: absolute;
  bottom: 0px;
}
#fader3 {
  height: 100%;
  position: absolute;
  left: 0px;
}
#fader4 {
  height: 100%;
  position: absolute;
  right: 0px;
}
.flrstart {
  width: 49.5%;
}
.flrend {
  width: 0%;
}
.ftbstart {
  height: 49.5%;
}
.ftbend {
  height: 0%;
}

#center {
  --navtxt: blue;
  --dark-grad: radial-gradient(
    farthest-corner,
    rgba(255, 255, 255, 1) 0%,
    rgba(0, 0, 0, 1) 100%
  );
  position: absolute;
  background: var(--dark-grad);
  transition: background 1s 0s ease-out, height 1s 1s ease-out,
    top 1s 1s ease-out, width 0.5s 0s ease-in-out, left 0.5s 0s ease-in-out,
    opacity 2.5s 0.5s ease-in-out;
}
.centerStart {
  width: 1%;
  height: 1%;
  left: 49.5%;
  top: 49.5%;
  opacity: 100%;
}
.centerEnd {
  width: 100%;
  height: 100%;
  left: 0%;
  top: 0%;
  opacity: 0%;
}
.dark {
  background: black;
  transition: background 1s 0s ease-out, height 1s 1s ease-out,
    top 1s 1s ease-out, bottom 1s 1s ease-out, width 0.5s 0s ease-in-out,
    left 0.5s 0s ease-in-out, right 0.5s 0s ease-in-out,
    opacity 2s 0.5s ease-in-out;
}
</style>
