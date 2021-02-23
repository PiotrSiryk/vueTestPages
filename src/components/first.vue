<template>
  <div>
    <Second />
  </div>
</template>

<script>
import Second from "./second.vue";
// import Third from "./second.vue";
export default {
  data() {
    return { arg: " pies" };
  },
  components: {
    Second,
  },
  methods: {
    doStuff: function() {},
  },
};
</script>

<style lang="scss" scoped></style>
