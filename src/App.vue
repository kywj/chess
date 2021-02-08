<template>
  <div>
    <div>n 的值为 {{ n }}</div>
    <div class="row">
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
    </div>
    <div class="row">
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
    </div>
    <div class="row">
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
      <Cell @click="onClickCell" :n="n" />
    </div>
  </div>
</template>

<script>
import Cell from "./Cell.vue";
export default {
  components: { Cell },
  data() {
    return {
      n: 0,
    };
  },
  methods: {
    onClickCell() {
      console.log("某个 Cell 被点击了");
      this.n += 1;
    },
  },
};
</script>

<style scoped>
.row {
  display: flex;
}
</style>
