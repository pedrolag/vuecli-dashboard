<template>
  <div class="navbar"></div>
</template>

<script>
export default {
  name: "Navbar",
  props: {},
  data: () => {
    return {};
  },
};
</script>

<style scoped lang="scss">
.navbar {
  width: $navbar-width;
  height: $navbar-height;
  background: $navbar-background;
  border-bottom: $navbar-border;
}
</style>
