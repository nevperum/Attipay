<template>
  <div><Topbar /> <Order /></div>
</template>

<script>
import Topbar from "./components/Topbar.vue";
import Order from "./components/Order.vue";
export default {
  name: "App",
  components: {
    Topbar,
    Order,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1b3957;
  margin-top: 60px;
  background: #f5f9fc;
}

html,
body {
  margin: 0;
  padding: 0;
}
</style>