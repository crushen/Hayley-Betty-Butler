<template>
  <div id="home">
    <div class="background-container" :style="{backgroundImage: `url(${backgroundMobile})`}">
      <h1>Hayley<br>Betty Butler</h1>
    </div>

    <div style="height: 500px"></div>
  </div>
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
    z-index: -20;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  h1 {
    color: white;
    font-size: 55px;
  }
  
</style>