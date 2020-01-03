<template>
  <div class="home">
    <landing/>
    <collections/>
  </div>
</template>

<script>
import Landing from '@/components/Landing.vue';
import Collections from '@/components/collections/Collections.vue';

export default {
  name: 'home',
  components: {
    Landing,
    Collections
  }
}
</script>