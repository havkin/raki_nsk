<template>
  <div class="layoutContainer">
    <Header />
    <CatalogMobile />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./Header.vue";
import Footer from "./Footer.vue";
import Main from "./Main.vue";
import CatalogMobile from "@/components/Catalog/CatalogMobile.vue";

export default {
  name: "Layout",
  components: {
    Header,
    Footer,
    Main,
    CatalogMobile,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/global.scss";

  .layoutContainer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    /* max-width: 1280px; */
    margin: 0 auto;
    padding: 0 10px;
    height: 100vh;

    @media (min-width: $MOBILE) {
      padding: 0 60px;
    }
  }
</style>
