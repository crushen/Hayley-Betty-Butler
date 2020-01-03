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
:root {
  --background: #171717;
}

* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: 'Muli', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  background: var(--background);
}

p {
  font-size: 18px;
  line-height: 28px;
}

a {
  text-decoration: none;
}

.content {
  width: 85%;
  margin: auto;
}

.section-padding {
  padding: 60px 0;
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
