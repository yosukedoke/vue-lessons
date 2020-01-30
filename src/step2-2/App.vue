<template>
  <div id="app">
    <div class="todos">
      <section class="todo-item">
        <h2 class="todo-item__content">1. TODO false</h2>
      </section>
      <section class="todo-item">
        <h2 class="todo-item__content">2. TODO false</h2>
      </section>
      <section class="todo-item">
        <h2 class="todo-item__content">3. TODO true</h2>
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
        {
          id: 1,
          content: "起きる",
          isDone: false
        },
        {
          id: 2,
          content: "歯を磨く",
          isDone: false
        },
        {
          id: 3,
          content: "朝食を作る",
          isDone: false
        },
        {
          id: 4,
          content: "朝食を食べる",
          isDone: false
        },
        {
          id: 5,
          content: "服を着替える",
          isDone: false
        }
      ]
    };
  }
};
</script>
<style scoped>
#app {
  padding: 24px;
}
.todo-item {
  padding: 8px 12px;
}
.todo-item + .todo-item {
  border-top: 1px solid #f0f0f0;
}
.todo-item__content {
  font-size: 14px;
  line-height: 24px;
  margin: 0;
}
</style>
