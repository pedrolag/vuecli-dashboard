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
</style>
