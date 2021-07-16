<template>
  <div id="nav">
    <div class="navbar"></div>
    <div class="sidenav">
      <ul>
        <li v-for="objModule in arrModules" :key="objModule.id">
          <a href="objModule.url">
            <i>{{ objModule.icon }}</i>
            {{ objModule.name }}
          </a>
        </li>
        <li v-for="x in 20" :key="x">
          <a href="objModule.url">
            <i>bla</i>
            x bla
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {},
  data: () => {
    return {
      arrModules: [
        {
          id: 0,
          name: "Home",
          icon: "home",
          url: "",
        },
        {
          id: 1,
          name: "Colors",
          icon: "tint",
          url: "",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#nav {
  width: 100vw;
  height: 100vh;

  .navbar {
    width: $navbar-width;
    height: $navbar-height;
    background: $navbar-background;
    border-bottom: $navbar-border;
  }

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
        @include sidenav-hover-color($color-sidenav-button-hover, .1);
      }
    }
  }
}
</style>
