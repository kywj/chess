<template>
  <div>
    <div class="cell" id="app" v-on:click="a = true">
      <template v-if="a">{{ text }}</template>
      <template v-else></template>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { a: false, text: "o" };
  },
};
</script>

<style scoped>
.cell {
  border: 1px solid black;
  width: 100px;
  height: 100px;
  font-size: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
