<template>
  <div class="screen">Screen Component</div>
</template>

<script>
export default {
  name: "Screen",
};
</script>

<style scoped>
.screen {
  scroll-snap-align: start;
  width: 100%;
  height: 100%;
}
</style>
