<template>
  <Layout />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Header from './components/Header.vue'
import Layout from './components/Layout.vue'

export default defineComponent({
  name: 'App',
  components: {
    Layout,
  }
})
</script>

<style lang="scss">
  @import "./assets/reset.scss";
</style>
