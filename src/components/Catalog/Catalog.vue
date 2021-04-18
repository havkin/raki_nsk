<template>
  <div>
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
import {data} from '../../assets/stub_data/catalog';
export default {
  name: "Catalog",
  data() {
    return {data}
  },
  methods: {
    handler(item) {
      console.log(item);
    }
  }
};
</script>

<style lang="scss" scoped>
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
