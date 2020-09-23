<template>
  <div class="welcome">Hi!</div>
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
  background-image: url("../assets/test1.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: top;

  /* background-size: cover;
  background-position-x: left;
  background-position-y: top; */

  /* color: black; */
}
</style>
