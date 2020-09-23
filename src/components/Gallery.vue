<template>
  <div class="gallery screen">
    <div class="item" @click="showItem(1)">1</div>
    <div class="item" @click="showItem(2)">2</div>
    <div class="item" @click="showItem(3)">3</div>
    <div class="item" @click="showItem(4)">4</div>
  </div>
</template>

<script>
export default {
  name: "Gallery",
  methods: {
    showItem: function(item) {
      console.log("item", item);
      this.$emit("showItem");
    },
  },
};
</script>

<style scoped>
.gallery {
  /* background: url("../assets/dots.svg"); */
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
.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background: grey;
  z-index: 100;
}

.screen {
  scroll-snap-align: start;
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
}
</style>
