<template>
  <div id="app">
    <app-title>{{ title }}</app-title>
    <p>{{ count }} / {{ countPerPage }} counts</p>
    <p>{{ numPage }} pages</p>
    <!-- <display-pagination :count="count" :count-per-page="countPerPage" /> -->
    <button @click="onClickUp">Up</button>
  </div>
</template>
<script>
import AppTitle from "./components/AppTitle";
// import DisplayPagination from './components/DisplayPagination'

export default {
  name: "App",
  components: {
    AppTitle,
    // DisplayPagination,
  },
  data() {
    return {
      title: "Hello! Vue!",
      count: 0,
      countPerPage: 5
    };
  },
  computed: {
    numPage() {
      return Math.floor(this.count / this.countPerPage) + 1;
    }
  },
  methods: {
    onClickUp() {
      this.count++;
    }
  }
};
</script>
<style>
#app {
  padding: 24px;
}
</style>
