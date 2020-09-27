<template>
  <div class="welcome">
    <!-- <div class="topspace"></div> -->
    <div class="sides">
      <div class="banner"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome",
};
</script>

<style scoped>
.welcome {
  scroll-snap-align: start;
  width: 100%;
  min-height: 100%;
  background-color: black;
  /* background-image: url("../assets/hexadots-dark.svg"); */

  /* background-size: cover;
  background-position-x: left;
  background-position-y: top; */

  /* color: black; */
}
.topspace {
  height: 5vh;
}
.sides {
  background-color: white;
  height: 95vh;
}
.banner {
  background-color: white;
  background-image: url("../assets/test1.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: top;
  max-height: 100vmin;
  max-width: 190vmin;
  height: 100%;
  margin: auto;
}
</style>
