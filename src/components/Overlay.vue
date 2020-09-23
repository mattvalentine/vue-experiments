<template>
  <div class="overlay" v-show="show" @click="unshow">Overlay</div>
</template>

<script>
export default {
  name: "Overlay",
  props: ["show"],
  methods: {
    unshow: function() {
      this.show = false;
    },
  },
};
</script>

<style scoped>
.overlay {
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  background: gray;
}
</style>
