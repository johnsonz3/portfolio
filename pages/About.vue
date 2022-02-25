<template>
  <div>
    <Navbar/>
    <About/>
  </div>
</template>

<script>
import About from '../layouts/about.vue';
import Navbar from '../layouts/navbar.vue';
export default {
  name: 'InspirePage',
  components: {
    Navbar,
    About,
  }
}
</script>
