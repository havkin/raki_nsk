<template>
  <div class="mainContent">
    <Catalog />
    <Board />
  </div>
</template>

<script>
import Catalog from "./Catalog.vue";
import Board from "./Board.vue";

export default {
  name: "Main",
  components: {
    Catalog,
    Board,
  },
};
</script>

<style lang="scss" scoped>
  .mainContent {
    display: flex;
    flex-grow: 2;
    background-color: #eee;
  }
</style>
