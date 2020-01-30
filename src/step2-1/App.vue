<template>
  <div id="app">
    <div class="todos">
      <section>
        <p>TODO</p>
      </section>
      <section>
        <p>TODO</p>
      </section>
      <section>
        <p>TODO</p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      todos: []
    };
  }
};
</script>
<style scoped>
#app {
  padding: 24px;
}
</style>
