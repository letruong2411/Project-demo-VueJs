<template>
  <div id="app">
    <ComponentHeader />
    <ManageProducts />
  </div>
</template>

<script>
import ComponentHeader from "./components/ComponentHeader";

import ManageProducts from "./components/ManageProducts";
export default {
  created() {},
  methods: {},
  name: "App",
  components: {
    ComponentHeader,
    ManageProducts,
  },
};
</script>

<style>
#app {
  font-family: "Times New Roman", Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
