<template>
  <vue-scroll-snap>
    <Navbar/>
    <div v-if="window.width >= 480" class="item">
      <skillsList/>
    </div>
    <div v-else class="item">
      <skillsListAlt/>
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
import skillsListAlt from '../layouts/skillsListAlt.vue';
import VueScrollSnap from "vue-scroll-snap";

export default {
  name: 'SkillsPage',
  components: {
    Navbar,
    FooterSection,
    skillsList,
    VueScrollSnap,
    skillsListAlt
  },
  data () {
    return{
        window: {
            width: 0,
            height: 0
        }
    }
    },
    created() {
        window.addEventListener('resize', this.handleResize);
        this.handleResize();
    },
    destroyed() {
        window.removeEventListener('resize', this.handleResize);
    },
    methods: {
        handleResize() {
            this.window.width = window.innerWidth;
            this.window.height = window.innerHeight;
        }
    }
}
</script>
