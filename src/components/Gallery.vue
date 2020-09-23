<template>
  <div class="gallery screen">
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
  /* background: url("../assets/dots.svg"); */
  display: flex;
  align-items: center;
  justify-content: center;
  align-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  /* flex-basis: 40vmin; */
}
.item {
  color: yellow;
  width: 40vmin;
  height: 40vmin;
  background: red;
  margin: 2.5vmin;
  cursor: pointer;
  flex-shrink: 1;
  /* flex-grow: 1; */
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
  min-height: 100%;
  top: 0px;
  left: 0px;
}
</style>
