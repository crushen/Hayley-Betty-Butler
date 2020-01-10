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

h1 {
  text-transform: uppercase;
  font-size: 14px;
}

.line {
  height: 1px;
  width: 100%;
  background: var(--text);
  margin: 16px 0 60px 0;
}

h2 {
  font-size: 18px;
  font-weight: bold;
}

.collection {
  padding-bottom: 32px;
  position: relative;
  z-index: 10;
  background: var(--background);
}

.sub-title {
  margin-top: 14px;
  font-weight: bold;
}

.description {
  font-size: 14px;
  margin: 32px 0 60px 0;
  font-style: italic;
}

.gallery {
  margin-top: 60px;
}

img {
  width: 100%;
}

.img-title {
  font-weight: bold;
  margin: 16px 0 6px 0;
}

.img-description {
  font-size: 14px;
}

button {
  font-family: 'Muli', sans-serif;
  outline: none;
  border: none;
  background: white;
  padding: 6px;
  text-transform: uppercase;
  border-radius: 3px;
  margin-top: 8px;
}

</style>