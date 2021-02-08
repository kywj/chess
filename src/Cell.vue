<template>
  <div>
    {{ n }}
    <div class="cell" id="app" v-on:click="onClickSelf">
      <template v-if="a">{{ text }}</template>
      <template v-else></template>
    </div>
  </div>
</template>

<script>
export default {
  props: ["n"],
  data() {
    return { a: false, text: "" };
  },
  methods: {
    onClickSelf() {
      if (this.text !== "") return;
      this.a = true;
      this.text = this.n % 2 === 0 ? "x" : "o";
      this.$emit("click");
    },
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
