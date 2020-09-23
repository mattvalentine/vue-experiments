<template>
  <div class="gallery">
    <div class="item" v-for="item in items" :key="item" @click="showItem(item)">
      {{ item }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Gallery",
  data: function() {
    return {
      items: [1, 2, 3, 4, 5, 6, "seven", "VIII"],
    };
  },
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
  scroll-snap-align: start;
  width: 100%;
  min-height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  align-content: center;
  flex-direction: row;
  flex-wrap: wrap;
}
.item {
  color: yellow;
  width: 40vmin;
  height: 40vmin;
  background: red;
  margin: 2.5vmin;
  cursor: pointer;
}
.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background: grey;
  z-index: 100;
}
</style>
