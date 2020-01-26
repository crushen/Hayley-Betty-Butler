<template>
  <section id="solo-pieces" class="section">
    <div class="content">

      <div class="title">
        <h1>Solo Pieces</h1>
        <div class="line"></div>
      </div>

      <div class="wrapper">
        <div class="solo-piece gallery" v-for="piece in soloPieces" :key="piece.id">
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

export default {
  apollo: {
    soloPieces: {
      query: soloPieces
    }
  }
}
</script>

<style scoped>
@media screen and (min-width: 700px) {
  .section {
    padding-top: 60px;
  }
  
  .wrapper {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-content: space-between;
  }

  .solo-piece.gallery {
    width: 45%;
    max-width: 300px;
    flex: 1 0 auto;
  }
}


</style>