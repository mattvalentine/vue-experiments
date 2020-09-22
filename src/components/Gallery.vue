<template>
  <div class="gallery screen">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </div>
</template>

<script>
export default {
  name: "Gallery",
};
</script>

<style scoped>
.gallery {
  display: flex;
  align-items: center;
  justify-content: center;
  align-content: center;
  flex-wrap: wrap;
}
.item {
  color: yellow;
  width: 40vmin;
  min-height: 40vmin;
  background: red;
  margin: 2.5vmin;
}

.screen {
  scroll-snap-align: start;
  width: 100%;
  height: 100%;
}
</style>
