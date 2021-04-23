<template>
  <div class="layoutContainer">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./Header.vue";
import Footer from "./Footer.vue";
import Main from "./Main.vue";

export default {
  name: "Layout",
  components: {
    Header,
    Footer,
    Main,
  },
};
</script>

<style lang="scss" scoped>
  .layoutContainer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    /* max-width: 1280px; */
    margin: 0 auto;
    padding: 0 60px;
    height: 100vh;
  }
</style>
