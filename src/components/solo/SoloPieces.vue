<template>
  <section id="solo-pieces" class="section">
    <div class="content">

      <div class="title">
        <h1>Solo Pieces</h1>
        <div class="line"></div>
      </div>

      <div class="wrapper">
        <div 
          v-for="piece in soloPieces" 
          :key="piece.id"
          class="solo-piece gallery">
          <img :src="piece.image.url" alt="">
          <p class="img-title">{{ piece.title }}</p>
          <p class="img-description">{{ piece.description }}</p>
          <a href="mailto:hayley.butler83@gmail.com"><button>Enquire</button></a>
        </div>          
      </div>
    </div>
  </section>
</template>

<script>
import gql from 'graphql-tag';

const soloPieces = gql`
  query {
    soloPieces {
      title,
      description
      image {
        url
      }
    }
  }
`

// 1  2  3
// 4  5  6
// 7  8  9
// 10 11 12
// 13 14 15
// 16 17 18
// 19 20 21
// 22 23 24
// 25 26 27
// 28 29 30

// slice first 3 items from array

export default {
  apollo: {
    soloPieces: {
      query: soloPieces
    }
  },
  data() {
    return {
    }
  }
}
</script>

<style scoped>
@media screen and (min-width: 700px) {
  /* .section {
    padding-top: 60px;
  }
  */
  
  .wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    align-items: flex-start;
  }

  .solo-piece.gallery {
    width: 45%;
    max-width: 300px;
    display: inline-block;
  }

}

@media screen and (min-width: 1100px) {

}


</style>