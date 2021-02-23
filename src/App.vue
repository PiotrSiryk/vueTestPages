<template>
  <div>
    <div id="app">
      <div v-for="(el, index) in filteredList" v-bind:key="index">
        {{ el.id }}. {{ el.name }}
      </div>
      <button
        class="btn"
        v-for="el in Math.ceil(arr.length / elementsOnPage)"
        v-bind:key="el * 100"
        v-bind:class="{ 'btn-active': currentPage === el }"
        v-on:click="currentPage = el"
      >
        {{ el }}
      </button>
    </div>
  </div>
</template>

<script>
//import First from "./components/first";

export default {
  name: "App",
  data() {
    return {
      currentPage: 1,
      elementsOnPage: 5,
      arr: [
        { id: 1, name: "item one" },
        { id: 2, name: "item two" },
        { id: 3, name: "item three" },
        { id: 4, name: "item four" },
        { id: 5, name: "item five" },
        { id: 6, name: "item six" },
        { id: 7, name: "item one" },
        { id: 8, name: "item two" },
        { id: 9, name: "item three" },
        { id: 10, name: "item four" },
        { id: 11, name: "item five" },
        { id: 12, name: "item six" },
        { id: 1, name: "item one" },
        { id: 2, name: "item two" },
        { id: 3, name: "item three" },
        { id: 4, name: "item four" },
        { id: 5, name: "item five" },
        { id: 6, name: "item six" },
        { id: 7, name: "item one" },
        { id: 8, name: "item two" },
        { id: 9, name: "item three" },
        { id: 10, name: "item four" },
        { id: 11, name: "item five" },
        { id: 12, name: "item six" },
      ],
    };
  },
  computed: {
    filteredList() {
      const filtered = this.arr.filter(
        (el, index) =>
          Math.ceil((index + 1) / this.elementsOnPage) === this.currentPage
      );
      console.log(filtered);
      return filtered;
    },
  },
};
</script>

<style>
#app {
  text-align: center;
}
.btn {
  width: 40px;
  height: 40px;
  margin: 5px;
}
.btn-active {
  background-color: rgb(94, 94, 255);
}
.parColor {
  color: red;
  background-color: bisque;
}
</style>
