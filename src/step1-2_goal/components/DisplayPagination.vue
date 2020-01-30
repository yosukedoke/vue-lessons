<template>
  <div>
    <p>{{ count }} / {{ countPerPage }} counts</p>
    <p>{{ numPage }} pages</p>
  </div>
</template>
<script>
export default {
  name: "DisplayPagination",
  props: {
      count: Number,
      countPerPage: Number
  },
  computed: {
    numPage() {
      return Math.floor(this.count / this.countPerPage) + 1;
    }
  }
};
</script>

