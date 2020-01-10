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

.title h1 {
  text-transform: uppercase;
  font-size: 14px;
}

.line {
  height: 1px;
  width: 100%;
  background: var(--text);
  margin: 16px 0 60px 0;
}

h2 {
  font-size: 18px;
  font-weight: bold;
}

.collection, .solo-piece {
  padding-bottom: 32px;
  position: relative;
  z-index: 10;
  background: var(--background);
}

.collection:last-of-type, .solo-piece:last-of-type {
  padding-bottom: 0;
}

.sub-title {
  margin-top: 14px;
  font-weight: bold;
}

.description {
  font-size: 14px;
  margin: 32px 0 60px 0;
  font-style: italic;
}

.gallery {
  margin-top: 60px;
}

img {
  width: 100%;
}

.img-title {
  font-weight: bold;
  margin: 16px 0 6px 0;
}

.img-description {
  font-size: 14px;
}

button {
  font-family: 'Muli', sans-serif;
  outline: none;
  border: none;
  background: white;
  padding: 6px;
  text-transform: uppercase;
  border-radius: 3px;
  margin-top: 8px;
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
