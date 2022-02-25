<template>
  <div>
    <Navbar/>
    <FooterSection/>
  </div>
</template>

<script>
import Navbar from '../layouts/navbar.vue';
import FooterSection from '../layouts/FooterSection.vue';
export default {
  name: 'SkillsPage',
  components: {
    Navbar,
    FooterSection
  }
}
</script>
