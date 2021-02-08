<template>
  <div>
    <div class="row">
      <Cell />
      <Cell />
      <Cell />
    </div>
    <div class="row">
      <Cell />
      <Cell />
      <Cell />
    </div>
    <div class="row">
      <Cell />
      <Cell />
      <Cell />
    </div>
  </div>
</template>

<script>
import Cell from "./Cell.vue";
export default {
  components: { Cell },
};
</script>

<style scoped>
.row {
  display: flex;
}
</style>
