<template>
  <section class="todo-item">
    <h2 class="todo-item__content">1. TODO false</h2>
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
</style>
