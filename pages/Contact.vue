<template>
  <div>
    <Navbar/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from '../layouts/navbar.vue';
import Footer from '../layouts/Footer.vue';
export default {
  name: 'ContactPage',
  components: {
    Navbar,
    Footer
  }
}
</script>
