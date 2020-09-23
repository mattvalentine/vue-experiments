<template>
  <div class="container">
    <div class="title"><h1>Footer</h1></div>
    <div class="screen">Footer stuff</div>
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
  /* min-height: 90%; */
}
.container {
  width: 100%;
  min-height: 50%;
  scroll-snap-align: end;
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
