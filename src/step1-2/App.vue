<template>
  <div id="app">
    <app-title>{{ title }}</app-title>
    <p>12 / 5 counts</p>
    <p>3 pages</p>
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
      title: "Hello! Vue!"
    };
  }
};
</script>
<style>
#app {
  padding: 24px;
}
</style>
