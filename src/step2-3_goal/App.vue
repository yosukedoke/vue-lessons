<template>
  <div id="app">
    <todo-item v-for="todo in todos" :key="todo.id" :todo="todo" @change-todo="onChangeTodo"/>
    <todos-progress :num-total="numTodos" :num-done="numDone"/>
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
    numDone() {
      return this.todos.filter(todo => todo.isDone).length;
    },
    numTodos() {
      return this.todos.length;
    },
  },
  methods: {
    onChangeTodo(newTodo) {
      console.log(newTodo);
      const indexAt = this.todos.findIndex(todo => todo.id === newTodo.id);
      this.todos.splice(indexAt, 1, newTodo);
    }
  }
};
</script>
<style scoped>
#app {
  padding: 24px;
}
</style>