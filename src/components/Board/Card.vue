<template>
  <div class="cardContainer">
    <div class="cardImageWrapper">
      <img :src="data?.image" alt="card image" class="cardImage">
    </div>
    <div class="cardTitle">{{data?.title}}</div>
    <div class="cardPrice">{{data?.price}} руб/кг</div>
    <div>{{data?.catId}}</div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    data: Object,
  },
  computed: {
    imagePath() {
      return "food.jpg"
    }
  }
}
</script>

<style lang="scss" scoped>
  .cardContainer {
    min-width: 300px;
    max-width: 500px;
    border: 1px solid black;
    border-radius: 5px;
    margin-bottom: 24px;
    background-color: #fff;
  }
  .cardImage {
    width: 100%;
    height: 300px;
    object-fit: cover;
  }
  .cardTitle {
    padding: 10px;
    font-size: 2rem;
  }
  .cardPrice {
    padding: 10px;
    font-size: 1.5rem;
  }
</style>