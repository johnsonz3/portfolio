<template>
  <div >
    <Navbar/>
    <About/>
    <FooterSection/>
  </div>
</template>

<script>
import About from '../layouts/about.vue';
import Navbar from '../layouts/navbar.vue';
import FooterSection from '../layouts/FooterSection.vue';
export default {
  name: 'AboutPage',
  components: {
    Navbar,
    About,
    FooterSection
  }
}
</script>
