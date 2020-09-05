<template>
  <div class="screen slideholder">
    <div class="slide">Screen Component</div>
    <div class="slide">Screen Component</div>
  </div>
</template>

<script>
export default {
  name: "Slider",
};
</script>

<style>
.slideholder {
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap: nowrap;
  overflow-x: scroll;
}
.slide {
  flex-shrink: 0;
  width: 100%;
  height: 100%;
}
</style>
