<template>
  <nav class="navbar-large">
    <div class="nav-inner">
      <router-link to="/" exact>Home</router-link>
      <router-link to="/brands">Brands</router-link>
      <router-link to="/side-projects">Side Projects</router-link>
    </div>
  </nav>
</template>

<script>
</script>

<style scoped>
  nav {
    text-align: right;
    width: 100%;
    padding: 20px 0;
    position: fixed;
    top: 0;
    right: 0;
    z-index: 40;
    border-bottom: 3px solid transparent;
  }
  
  a {
    color: var(--secondary-text);
    border-bottom: 3px solid transparent;
    font-weight: 400;
    font-size: 15px;
    margin-left: 40px;
    cursor: pointer;
    transition: 0.25s;
  }
  a:hover {
    color: var(--main-text);
    border-bottom: 3px solid var(--main-text);
  }
  nav a.router-link-active {
    color: var(--main-text);
    border-bottom: 3px solid var(--main-text);
  }
  .nav-inner {
    max-width: 1050px;
    margin: auto; 
  }
</style>