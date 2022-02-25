<template>
  <div>
    <Navbar/>
    <Projects/>
    <FooterSection/>
  </div>
</template>

<script>
import Navbar from '../layouts/navbar.vue';
import Projects from '../layouts/projectList.vue';
import FooterSection from '../layouts/FooterSection.vue';
export default {
  name: 'ProjectPage',
  components: {
    Navbar,
    Projects,
    FooterSection
  }
}
</script>