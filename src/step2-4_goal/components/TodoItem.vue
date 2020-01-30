<template>
  <section :class="classes" @click="onClick">
    <span class="todo-item__id">{{todo.id}}.</span>
    <h2 class="todo-item__content">{{todo.content}}</h2>
    <span class="todo-item__status">{{displayStatus}}</span>
  </section>
</template>

<script>
export default {
  name: "TodoItem",
  props: {
    todo: {
      type: Object,
      required: true
    }
  },
  computed: {
    classes() {
      return [
        'todo-item',
        { 'is-done': this.todo.isDone }
      ];
    },
    displayStatus() {
      return this.todo.isDone ? "済" : "未";
    }
  },
  methods: {
    onClick() {
      const isDone = !this.todo.isDone;
      const newTodo = {
        ...this.todo,
        isDone
      };
      this.$emit("change-todo", newTodo);
    }
  }
};
</script>
<style scoped>
.todo-item {
  padding: 8px 12px;
  display: flex;
  font-size: 14px;
}
.todo-item + .todo-item {
  border-top: 1px solid #f0f0f0;
}
.todo-item__content {
  flex-grow: 1;
  font-size: 14px;
  line-height: 24px;
  margin: 0;
}
.todo-item__id {
  font-size: 14px;
  line-height: 24px;
}
.todo-item__status {
  font-size: 14px;
  line-height: 24px;
}
.todo-item.is-done {
  color: #999;
  background: #f4f4f4;
}
.todo-item.is-done > .todo-item__status {
  color: #3c6;
}
</style>
