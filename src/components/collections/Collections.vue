<template>
  <section id="collections" class="section">
    <div class="content">

      <div class="title">
        <h1>Collections</h1>
      </div>

      <div class="collection" v-for="col in collections" :key="col.id">
        <div class="line"></div>
        <h2>{{ col.title }}</h2>
        <p class="sub-title">{{ col.subTitle }}</p>
        <p class="description">{{ col.description }}</p>

        <div class="gallery" v-for="img in col.galleryItems" :key="img.id">
          <img :src="img.image.url" alt="">
          <p class="img-title">{{ img.title }}</p>
          <p class="img-description">{{ img.description }}</p>
          <button>Enquire</button>
        </div>

      </div>

    </div>
  </section>
</template>

<script>
import gql from 'graphql-tag';

const collections = gql`
  query {
    collections {
      id
      title
      subTitle
      description
      galleryItems(orderBy: sort_ASC) {
        id
        title
        description
        image {
          url
        }
      }
    }
  }
`

export default {
  apollo: {
    collections: {
      query: collections
    }
  }
}
</script>

<style scoped>


</style>