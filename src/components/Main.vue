<template>
  <div class="mainContent">
    <Catalog />
    <Board />
  </div>
</template>

<script>
import Catalog from "./Catalog/Catalog.vue";
import Board from "./Board/Board.vue";

export default {
  name: "Main",
  components: {
    Catalog,
    Board,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/global.scss";

  .mainContent {
    display: flex;
    flex-grow: 2;
    background-color: #eee;
    overflow-y: scroll;
    flex-direction: column;
    padding: 10px;

    @media (min-width: $MOBILE) {
      flex-direction: row;
    }
  }
</style>
