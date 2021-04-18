<template>
  <div class="boardContainer">
    <Card 
      v-for="card in data"
      :key="card"
      :data="card"
    />
  </div>
</template>

<script>
import Card from "./Card.vue";
import {data} from "@/assets/stub_data/cards";

export default {
  name: "Board",
  components: {
    Card,
  },
  data() {
    return {data}
  },
};
</script>

<style lang="scss" scoped>
  .boardContainer {
    display: flex;
    flex-wrap: wrap;
  }
</style>
