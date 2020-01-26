<template>
  <section id="solo-pieces" class="section">
    <div class="content">

      <div class="title">
        <h1>Solo Pieces</h1>
        <div class="line"></div>
      </div>

      <div class="solo-piece gallery" v-for="piece in soloPieces" :key="piece.id">
        <img :src="piece.image.url" alt="">
        <p class="img-title">{{ piece.title }}</p>
        <p class="img-description">{{ piece.description }}</p>
        <button>Enquire</button>
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


</style>