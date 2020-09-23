<template>
  <div class="container">
    <div class="title"><h1>Title</h1></div>
    <div class="slideholder">
      <div class="slide" v-for="slide in slides" :key="slide">{{ slide }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider",
  data: function() {
    return {
      slides: ["A", "B", "C", "D"],
    };
  },
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 100%;
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

.slideholder {
  display: flex;
  flex-wrap: nowrap;
  overflow-x: scroll;
  scroll-snap-type: x proximity;
  scroll-behavior: smooth;
  height: 90%;
}
.slide {
  scroll-snap-align: center;
  flex-shrink: 0;
  width: 100%;
  height: 100%;
}
</style>
