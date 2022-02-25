<template>
  <div>
    <Navbar/>
    <Projects/>
  </div>
</template>

<script>
import Navbar from '../layouts/navbar.vue';
import Projects from '../layouts/projectList.vue';
export default {
  name: 'InspirePage',
  components: {
    Navbar,
    Projects,
  }
}
</script>