<template>
  <div class="boardContainer">
    <Card 
      v-for="card in filtredData"
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
  computed: {
    filtredData() {
      const catId = this.$route.query.catId || "all";
      if (catId == "all") return this.data;
      return this.data.filter(item => item.catId === catId);
    },
  },
};
</script>

<style lang="scss" scoped>
  .boardContainer {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: flex-start;
    padding-top: 30px;
  }
</style>
