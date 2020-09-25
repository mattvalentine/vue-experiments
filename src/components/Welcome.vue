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
}
.banner {
  background-color: white;
  background-image: url("../assets/test1.jpg");
  background-size: cover;
  /* background-repeat: no-repeat; */
  background-position-x: center;
  background-position-y: top;
  height: 70vh;
  max-width: 1000px;
  margin: auto;
}
</style>
