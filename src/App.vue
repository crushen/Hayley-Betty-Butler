<template>
  <div id="app">
    <mobile-nav id="mobile-nav"></mobile-nav>
    <app-nav id="nav"></app-nav>
    <router-view/>
  </div>
</template>

<script>
import MobileNav from "./components/nav/MobileNav.vue";
import AppNav from "./components/nav/Nav.vue";

export default {
  components: {
    MobileNav,
    AppNav
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

a {
  text-decoration: none;
}

/* Mobile */
#nav {
  display: none;
}

/*Desktop */
@media screen and (min-width: 1100px) {
  #mobile-nav {
    display: none;
  }
  #nav {
    display: block;
  }
}

</style>
