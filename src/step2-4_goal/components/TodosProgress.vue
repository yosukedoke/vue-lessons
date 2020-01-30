<template>
  <div :class="classes">
    <div>{{ displayProgress }}</div>
    <div class="todos-progress__bar" :style="progressWidth"></div>
  </div>
</template>
<script>
export default {
  name: "TodosProgress",
  props: {
    numDone: Number,
    numTotal: Number,
    isCompleted: Boolean
  },
  computed: {
    classes() {
      return [
        "todos-progress",
        { "is-completed": this.isCompleted }
      ];
    },
    percentOfDone() {
      return Math.round((this.numDone / this.numTotal) * 100);
    },
    displayProgress() {
      return `Progress: ${this.numDone}/${this.numTotal} (${
        this.percentOfDone
      }%)`;
    },
    progressWidth() {
      return `width: ${this.percentOfDone}%`;
    },
  }
};
</script>
<style scoped>
.todos-progress {
  background: #f0f0f0;
  padding: 8px 12px;
  font-size: 13px;
  line-height: 24px;

  position: relative;
  z-index: 0;
}
.todos-progress__bar {
  content: "";
  display: block;
  background: #fc9;

  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
}
.todos-progress.is-completed > .todos-progress__bar {
  background: #8eC;
}
</style>
