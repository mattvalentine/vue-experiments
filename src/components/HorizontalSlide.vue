<template>
  <div class="slideholder">
    <div class="slide red">Screen Component</div>
    <div class="slide blue">Screen Component</div>
    <div class="slide red">Screen Component</div>
    <div class="slide blue">Screen Component</div>
    <div class="slide red">Screen Component</div>
    <div class="slide blue">Screen Component</div>
  </div>
</template>

<script>
export default {
  name: "Slider",
};
</script>

<style scoped>
.slideholder {
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap: nowrap;
  overflow-x: scroll;
  scroll-snap-type: x proximity;
  scroll-behavior: smooth;
  scroll-snap-align: start;
}
.slide {
  scroll-snap-align: start;
  flex-shrink: 0;
  width: 100%;
  height: 100%;
}

.red {
  background: red;
}

.blue {
  background: blue;
}
</style>
