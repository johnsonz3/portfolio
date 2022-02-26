<template>
  <div>
    <div class="page-title"><h2>Projects</h2></div>
    <div class="card-container">
    <Card cardtitle='ACNH Field Guide'
          cardimage='acnh.png'
          cardcontent="A full-stack web application that utilizes the public Animal Crossing API to keep track
of what animals users have caught"

          :cardlanguages=" [
                          {
                            name: 'Vue',
                          },
                          {
                            name: 'Firebase',
                          },
                          {
                            name: 'Tailwind',
                          }
                          ]"></Card>
     <Card cardtitle='Airline Web Application'
          cardimage='p2.jpeg'
          cardcontent="A full stack web application that
allows users to query, delete, add, and update flight information for airports in Canada"
          :cardlanguages=" [
                          {
                            name: 'PHP',
                            image: ''
                          },
                          {
                            name: 'MySQL',
                            image: ''
                          },
                          {
                            name: 'JavaScript',
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
    window.scrollTo(0.5,0.5);
    if (localStorage.getItem('reloaded')) {
        // The page was just reloaded. Clear the value from local storage
        // so that it will reload the next time this page is visited.
        localStorage.removeItem('reloaded');
    } else {
        // Set a flag so that we know not to reload the page twice.
        localStorage.setItem('reloaded', '1');
        location.reload();
    }
  },
  methods: {
    scrollAnimation() {
      gsap.timeline({
      scrollTrigger: {
        trigger: ".card",
      }
    })
    .from(".card", { y : outerWidth * 1})
    }
  },
  data () {
    return {
     
    }
  }
}
</script>
