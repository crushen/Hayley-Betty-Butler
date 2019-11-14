<template>
  <section id="home">
    <div class="background-container" :style="{backgroundImage: `url(${backgroundMobile})`}">
      <h1>Hayley<br>Betty Butler</h1>
    </div>
  </section>
</template>

<script>
import backgroundMobile from '../assets/background-mobile.png';

export default {
  data() {
    return {
      backgroundMobile
    }
  }
  
}
</script>

<style scoped>
  .background-container {
    width: 100%;
    height: 100vh;
    background-size: 126%;
    background-repeat: no-repeat;
    background-attachment: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    z-index: 0;
  }

  h1 {
    color: white;
    font-size: 55px;
    font-weight: 800;
    position: fixed;
    z-index: 0;
  }
  
</style>