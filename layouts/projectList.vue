<template>
  <div>
    <span class="Project-title"><h2>Projects</h2></span>
    <div class="card-container">
    <Card cardtitle='Animal Crossing Field Guide'
          cardimage='acnh.png'
          cardcontent='Odddd'
          :cardlanguages=" [
                          {
                            name: 'Vue',
                            image: ''
                          },
                          {
                            name: 'Firebase',
                            image: ''
                          },
                          {
                            name: 'Tailwind',
                            image: ''
                          }
                          ]"></Card>
     <Card cardtitle='Airline Web Application'
          cardimage='acnh.png'
          cardcontent='Odddd'
          :cardlanguages=" [
                          {
                            name: 'PHP',
                            image: ''
                          },
                          {
                            name: 'MySQL',
                            image: ''
                          }
                          ]"></Card>     
    </div>
    
  </div>
</template>

<script>
import Card from '~/components/Card';
import gsap from 'gsap';
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default {
  name: 'projectList',
  components: {
    Card,
  },
   mounted: function() {
    this.scrollAnimation();
  },
  methods: {
    scrollAnimation() {
      gsap.timeline({
      scrollTrigger: {
        trigger: ".card",
      }
    })
    .from(".card", { y : innerWidth * 0.5})
    }
  },
  data () {
    return {
     
    }
  }
}
</script>
