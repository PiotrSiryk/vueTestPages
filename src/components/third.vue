<template>
  <div>
    <button v-on:click="setSomeState">new btn</button>
    {{ someObj }}
  </div>
</template>

<script>
export default {
  name: "Third",
  data() {
    return { someState: this.someState };
  },
};
</script>

<style scoped>
div {
  display: flex;
  flex-direction: column;
}
</style>
