<template>
  <section id="home">
    <div class="background-container" :style="{backgroundImage: `url(${backgroundMobile})`}">
      <h1>Hayley<br>Betty Butler</h1>
    </div>
    <div class="section bio">
      <div class="content">
        <p>A South London artist, singer/songwriter. Working with a variety of mediums to create pieces of work that explore emotion, colour, texture and light.</p> 
        <p>Her art, words and music interrogate what it is to be human.</p>
      </div>
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
    font-size: 13vw;
    font-weight: 800;
    position: fixed;
    z-index: 0;
  }

  .bio {

    font-weight: bold;
  }

  p:not(:first-of-type) {
    margin-top: 16px;
  }
  
</style>