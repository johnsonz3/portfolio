<template>
  <div>
    <Navbar/>
    <Footer/>
  </div>
</template>

<script>
import Card from '~/components/Card'
import Navbar from '../layouts/navbar.vue';
import Footer from '../layouts/Footer.vue';
export default {
  name: 'IndexPage',
  components: {
    Card,
    Navbar,
    Footer
  }
}
</script>
