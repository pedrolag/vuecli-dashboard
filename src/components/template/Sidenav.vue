<template>
  <div class="sidenav">
    <ul>
      <li v-for="objModule in arrModules" :key="objModule.id">
        <router-link :to="objModule.path" tag="a">
          <span><font-awesome-icon :icon="objModule.icon" /></span>
          {{ objModule.name }}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
import router from "@/router/index";

export default {
  name: "Sidenav",
  props: {},
  data: () => {
    return {
      arrModules: router.options.routes,
    };
  },
};
</script>

<style scoped lang="scss">
.sidenav {
  width: $sidenav-width;
  height: $sidenav-height;
  background: $sidenav-background;
  border-right: $sidenav-border;
  overflow-y: auto;

  a {
    color: #fff;
    width: 100%;
    padding: 1em 2em 1em calc(2em - 4px);
    display: inline-block;
    border-left: solid 4px transparent;

    &:hover {
      @include sidenav-hover-color($color-sidenav-button-hover, 0.1);
    }

    span {
      display: inline-block;
      margin-right: 16px;
    }
  }
}
</style>
