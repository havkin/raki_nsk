<template>
  <div class="catalogContainer">
    <div @click="handler('')" class="title catalogItem">Каталог</div>
    <div 
      v-for="item in data" 
      :key="item" 
      class="catalogItem"
      @click="handler(item)"
    >
      {{item}}
    </div>
  </div>
</template>

<script>
import {data} from '@/assets/stub_data/catalog';

export default {
  name: "Catalog",
  data() {
    return {data}
  },
  methods: {
    handler(item) {
      this.$router.push({query: {catId: item}});
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/global.scss";

  .catalogContainer {
    width: 200px;
    position: sticky;
    top: 0;
    display: none;
    padding-right: 10px;

    @media (min-width: $MOBILE) {
      display: block;
    }
  }
  .title {
    background-color: rgb(214, 209, 140);
    font-weight: bold;
    justify-content: center;
  }
  .catalogItem {
    height: 30px;
    border: 1px solid black;
    border-radius: 4px;
    display: flex;
    align-items: center;
    padding-left: 10px;
    padding-right: 10px;
    cursor: pointer;
  }
</style>
