<template>
  <div id="app">
    <div class="todos">
      <section v-for="todo in todos" :key="todo">
        <p>{{todo}}</p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      todos: [
        "起きる",
        "歯を磨く",
        "朝食を作る",
        "朝食を食べる",
        "服を着替える"
      ]
    };
  }
};
</script>
<style scoped>
#app {
  padding: 24px;
}
</style>
