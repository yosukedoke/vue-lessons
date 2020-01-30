<template>
  <div class="todos-progress">
    <div>Progress: {{numDone}} / {{ numTotal }} : {{ percentOfDone }} %</div>
  </div>
</template>
<script>
export default {
  name: "TodosProgress",
  props: {
    numDone: Number,
    numTotal: Number
  },
  computed: {
    percentOfDone() {
      return Math.round((this.numDone / this.numTotal) * 100);
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
</style>
