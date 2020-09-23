<template>
  <div class="container">
    <div class="title"><h1>Title</h1></div>
    <div class="screen">Screen Component</div>
  </div>
</template>

<script>
export default {
  name: "Screen",
};
</script>

<style scoped>
.screen {
  width: 100%;
  min-height: 90%;
}
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
</style>
