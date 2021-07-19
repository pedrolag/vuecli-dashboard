<template>
  <div class="content">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "Content",
  props: {},
  data: () => {
    return {};
  },
};
</script>

<style scoped lang="scss">
.content {
  width: $content-width;
  height: $content-height;
  position: absolute;
  top: $content-top;
  left: $content-left;
  padding: 1em;
}
</style>
