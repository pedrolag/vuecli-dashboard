<template>
  <div id="app">
    <Template />
  </div>
</template>

<script>
import Template from "./components/Template.vue";

export default {
  name: "App",
  components: {
    Template,
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
