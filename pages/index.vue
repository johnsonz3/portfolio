<template>
  <div>
    <Navbar/>
    <div class="main-page">
      <div class="text-container">
        <vue-typed-js :typeSpeed="100" :smartBackspace="true" :backDelay="100" :strings="['Web Developer', 'Software Developer', 'Software Engineer']">
          <h1>Hello, my name is Johnson Zhang <span class="main-page-content-title"><br/>New Grad <span class="typing"></span><br/></span>Expected Graduation Date: April, 2022</h1>
        </vue-typed-js>
      </div>
    </div>
    <FooterSection/>
  </div>
</template>

<script>
import Card from '~/components/Card'
import Navbar from '../layouts/navbar.vue';
import FooterSection from '../layouts/FooterSection.vue';

export default {
  name: 'IndexPage',
  components: {
    Card,
    Navbar,
    FooterSection
  }
}
</script>
