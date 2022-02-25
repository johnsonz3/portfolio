<template>
  <div >
    <Navbar/>
    <!-- <About/> -->
    <Footer/>
  </div>
</template>

<script>
import About from '../layouts/about.vue';
import Navbar from '../layouts/navbar.vue';
import Footer from '../layouts/Footer.vue';
export default {
  name: 'AboutPage',
  components: {
    Navbar,
    About,
    Footer
  }
}
</script>
