<template>
  <div id="home">
    <div class="background-container" :style="{backgroundImage: `url(${backgroundMobile})`}">

    </div>
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
  }
  
</style>