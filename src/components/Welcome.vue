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
  background-color: lightblue;
  background-image: url("../assets/hexadots-dark.svg");
  color: black;
}
</style>
