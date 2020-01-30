<template>
  <div id="app">
    <app-title>{{ title }}</app-title>
  </div>
</template>
<script>
import AppTitle from "./components/AppTitle";

export default {
  name: "App",
  components: {
    AppTitle
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
