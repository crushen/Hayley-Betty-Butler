<template>
  <div class="home">
    <landing/>
    <bio/>
  </div>
</template>

<script>
// @ is an alias to /src
import Landing from '@/components/Landing.vue'
import Bio from '@/components/Bio.vue'

export default {
  name: 'home',
  components: {
    Landing,
    Bio
  }
}
</script>
