<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> --> 
    <galeria></galeria>
  </div>
</template>

<script>
// @ is an alias to /src
import Galeria from '@/components/Galeria.vue'

export default {
  name: 'home',
  components: {
   Galeria
  }
}
</script>
