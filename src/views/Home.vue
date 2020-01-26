<template>
  <div class="home">
    <landing/>
    <collections/>
    <solo-pieces/>
    <contact />
  </div>
</template>

<script>
import Landing from '@/components/Landing.vue';
import Collections from '@/components/collections/Collections.vue';
import SoloPieces from '@/components/solo/SoloPieces.vue';
import Contact from '@/components/Contact.vue';

export default {
  name: 'home',
  components: {
    Landing,
    Collections,
    SoloPieces,
    Contact
  }
}
</script>