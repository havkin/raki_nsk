<template>
  <div class="catalogContainer">
    <div @click="visibleHandler" class="title catalogItem">Каталог</div>
    <div v-if="isOpen" class="catalog">
      <div class="catalogItem" @click="handler('')">all</div>
      <div v-for="item in data" :key="item" class="catalogItem" @click="handler(item)">
        {{ item }}
      </div>
    </div>
  </div>
</template>

<script>
import { data } from "@/assets/stub_data/catalog";

export default {
  name: "CatalogMobile",
  data() {
    return {
      data, 
      isOpen: false,
    };
  },
  methods: {
    handler(item) {
      this.isOpen = false;
      this.$router.push({ query: { catId: item } });
    },
    visibleHandler() {
      this.isOpen = !this.isOpen;
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
  display: block;

  @media (min-width: $MOBILE) {
      display: none;
    }
}
.title {
  background-color: rgb(214, 209, 140);
  font-weight: bold;
  justify-content: center;
}
.catalog {
  position: absolute;
  background-color: rgb(250, 252, 149);
}
.catalogItem {
  width: 200px;
  height: 50px;
  border: 1px solid black;
  border-radius: 4px;
  display: flex;
  align-items: center;
  padding: 10px;
  cursor: pointer;
}
</style>
