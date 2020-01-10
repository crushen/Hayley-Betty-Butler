<template>
  <div>
    <div class="nav-bar"></div>
    <img :src="logo" alt="" class="logo">
    <div class="burger" @click="toggleNav">
      <div class="burger-bar"></div>
    </div>
    <transition name="slide" enter-active-class="animated slideInDown faster" leave-active-class="animated slideOutUp faster">
      <nav class="nav" v-if="navActive">
        <a href="#home" class="nav-link animated fadeInRight">Home</a>
        <a href="#collections" class="nav-link animated fadeInRight">Collections</a>
        <a href="#solo-pieces" class="nav-link animated fadeInRight">Solo Pieces</a>
        <a href="#contact" class="nav-link animated fadeInRight">Contact</a>
      </nav>
    </transition>
  </div>
</template>

<script>
import logo from '../../assets/logo4.svg';

export default {
  data() {
    return {
      navActive: false,
      logo
    }
  },
  methods: {
    toggleNav() {
      this.navActive = !this.navActive;
      if(this.navActive) {
        document.querySelector('.burger').classList.add('active');
        window.addEventListener('scroll', noScroll);
      } else {
        document.querySelector('.burger').classList.remove('active');
        window.removeEventListener('scroll', noScroll);
      }
    }
  },
  watch: {
    '$route'() {
      this.navActive = false;
      document.querySelector('.burger').classList.remove('active');
      window.removeEventListener('scroll', noScroll);
    }
  }
  
}
function noScroll() {
  window.scrollTo(0, 0);
}
</script>

<style scoped>
  .nav-link {
    animation-duration: 0.5s;
  }

  .nav-link:nth-of-type(1) {
    animation-delay: 0.3s;
  }

  .nav-link:nth-of-type(2) {
    animation-delay: 0.4s;
  }

  .nav-link:nth-of-type(3) {
    animation-delay: 0.5s;
  }

  .nav-link:nth-of-type(4) {
    animation-delay: 0.6s;
  }

  .logo {
    width: 60px;
    position: fixed;
    z-index: 30;
    top: 13px;
    left: 5%;
  }

  .nav-bar {
    position: fixed;
    top: 0;
    right: 0;
    width: 100%;
    height: 60px;
    z-index: 10;
    transition: 0.3s;
  }
  .burger {
    position: fixed;
    top: 0;
    right: 3%;
    width: 60px;
    height: 60px;
    cursor: pointer;
    background: rgba(0,0,0,0);
    transition: 0.4s;
    z-index: 30;
  }
  .burger-bar {
    width: 35px;
    height: 4px;
    background: white;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    transition: 0.4s;
  }
  .burger-bar:before,
  .burger-bar:after {
    content: '';
    width:35px;
    height: 4px;
    background: white;
    position: absolute;
    transition: 0.4s;
  }
  .burger-bar::before {
    top: -10px;
  }
  .burger-bar::after {
    top: 10px;
  }
  .burger.active .burger-bar {
    background: rgba(0,0,0,0);
  }
  .burger.active .burger-bar::before {
    top: 0;
    transform: rotate(-45deg);
  }
  .burger.active .burger-bar::after {
    top: 0;
    transform: rotate(45deg);
  }
  .nav {
    position: fixed;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: #0d0d0d;
    z-index: 20;
  }
  .nav a {
    font-size: 24px;
    font-weight: 600;
    color: white;
    border-bottom: 4px solid transparent;
    margin: 16px;
    border-bottom: 4px solid transparent;
    line-height: 40px;
    transition: 0.25s;
  }
  .nav a:hover {
    color: white;
    border-bottom: 4px solid white;
  }
  .nav a.router-link-active {
    color: white;
    border-bottom: 4px solid white;
  }
  @media screen and (min-width: 700px) {
    .nav a {
      font-size: 36px;
      margin: 20px;
    }
  }
</style>