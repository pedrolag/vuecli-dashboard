<template>
  <div id="template">
    <div class="navbar"></div>
    <div class="sidenav">
      <ul>
        <li v-for="objModule in arrModules" :key="objModule.id">
          <a href="objModule.url">
            <span><font-awesome-icon :icon="objModule.icon" /></span>
            {{ objModule.name }}
          </a>
        </li>
      </ul>
    </div>
    <div class="content">asd</div>
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
          icon: "user-secret",
          url: "",
        },
        {
          id: 1,
          name: "Colors",
          icon: "user-secret",
          url: "",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#template {
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
        @include sidenav-hover-color($color-sidenav-button-hover, 0.1);
      }

      span {
        display: inline-block;
        margin-right: 16px;
      }
    }
  }

  .content {
    width: $content-width;
    height: $content-height;
    position: absolute;
    top: $content-top;
    left: $content-left;
    padding: 1em;
  }
}
</style>
