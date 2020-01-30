<template>
  <div id="app">
    <div class="todos">
      <todo-item v-for="todo in todos" :key="todo.id" :todo="todo"/>
      <todos-progress :num-total="numTodos" :num-done="numDone"/>
    </div>
  </div>
</template>

<script>
import TodoItem from "./components/TodoItem";
import TodosProgress from "./components/TodosProgress";
import todos from "./data/todos";

export default {
  name: "App",
  components: {
    TodoItem,
    TodosProgress
  },
  data() {
    return {
      todos
    };
  },
  computed: {
    numTodos() { return 5 },
    numDone() { return 0 }
  },
  methods: {
  }
};
</script>
<style scoped>
#app {
  padding: 24px;
}
</style>