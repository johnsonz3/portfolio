<template>
  <vue-scroll-snap>
    <Navbar/>
    <div class="item">
    <skillsList/>
    </div>
    <!-- <div class="item">
    <section id="skills-summary">
      
    </section>
    </div> -->
    <FooterSection/>
  </vue-scroll-snap>
</template>
<style>

  .item {
    /* Set the minimum height of the items to be the same as the height of the scroll-snap-container.*/
    min-height: 500px;
  }

  .scroll-snap-container {
    height: auto;
    width: 100%;
  }
</style>
<script>
import Navbar from '../layouts/navbar.vue';
import FooterSection from '../layouts/FooterSection.vue';
import skillsList from '../layouts/skillsList.vue';
import VueScrollSnap from "vue-scroll-snap";

export default {
  name: 'SkillsPage',
  components: {
    Navbar,
    FooterSection,
    skillsList,
    VueScrollSnap
  }
}
</script>
