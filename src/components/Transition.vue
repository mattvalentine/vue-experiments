<template>
  <div class="transition" :style="bgstyle"></div>
</template>

<script>
export default {
  name: "Transition",
  props: ["start", "end"],
  computed: {
    bgstyle: function() {
      var gradstyle = {
        background:
          "linear-gradient(180deg, " +
          this.start.toString() +
          " 0%, " +
          this.end.toString() +
          " 100%)",
      };
      return gradstyle;
    },
  },
};
</script>

<style scoped>
.transition {
  height: 30px;
  width: 100%;
}
</style>
