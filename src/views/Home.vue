<template>
  <div class="home">
    <landing/>
    <collections/>
    <solo-pieces/>
  </div>
</template>

<script>
import Landing from '@/components/Landing.vue';
import Collections from '@/components/collections/Collections.vue';
import SoloPieces from '@/components/solo/SoloPieces.vue';

export default {
  name: 'home',
  components: {
    Landing,
    Collections,
    SoloPieces
  }
}
</script>