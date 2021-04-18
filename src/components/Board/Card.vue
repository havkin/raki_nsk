<template>
  <div class="cardContainer">
    <div class="cardImage">{{data.image}}</div>
    <div class="cardTitle">{{data.title}}</div>
    <div class="cardPrice">{{data.price}}</div>
    <div class="cardPrice">{{data.catId}}</div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    data: Object,
  },
}
</script>

<style lang="scss" scoped>
  .cardContainer {
    display: flex;
    flex-direction: column;
    min-width: 300px;
    border: 1px solid black;
    border-radius: 5px;
  }
</style>