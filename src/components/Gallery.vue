<template>
  <div class="container">
    <div class="title"><h1>Title</h1></div>
    <div class="gallery">
      <div
        class="item"
        v-for="item in items"
        :key="item"
        @click="showItem(item)"
      >
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Gallery",
  data: function() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
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
.container {
  width: 100%;
  /* height: 100%; */
  min-height: 100%;
  scroll-snap-align: start;
}
.title {
  height: 10%;
  margin: 0px;
}

.title > h1 {
  margin-block-start: 0px;
  margin-block-end: 0px;
  margin: 0px;
  font-size: 7.5vh;
}
.gallery {
  width: 100%;
  /* height: auto; */
  min-height: 90%;
  display: flex;
  align-items: center;
  justify-content: center;
  align-content: center;
  flex-direction: row;
  flex-wrap: wrap;
}
.item {
  color: white;
  width: 40vmin;
  height: 40vmin;
  background: darkgray;
  margin: 2.5vmin;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}
.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background: grey;
  z-index: 100;
}
</style>
