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
  --text: #FFF;
}

* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: 'Muli', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--text);
  background: var(--background);
}

p {
  font-size: 18px;
  white-space: pre-line;
}

a {
  text-decoration: none;
}

.section {
  padding-top: 80px;
  position: relative;
  z-index: 10;
  background: var(--background);
}

.content {
  width: 85%;
  margin: auto;
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
