<template>
  <div id="app">
    <Navbar />
    <Sidenav />
    <Content />
  </div>
</template>

<script>
import Navbar from "./components/template/Navbar.vue";
import Sidenav from "./components/template/Sidenav.vue";
import Content from "./components/template/Content.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Sidenav,
    Content,
  },
};
</script>

<style lang="scss">
#app {
  background: $color-background;
}
::-webkit-scrollbar {
  width: 8px;
}
::-webkit-scrollbar-track {
  background: $color-scrollbar-track;
}
::-webkit-scrollbar-thumb {
  background: $color-scrollbar-thumb;
}
::-webkit-scrollbar-thumb:hover {
  background: $color-scrollbar-thumb;
}
</style>
