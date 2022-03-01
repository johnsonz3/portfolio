<template>
  <div>
    <div class="page-title"><h2>Projects</h2></div>
    <div class="card-container">
       <!-- Project 0 -->
    <Card cardtitle='Personal Website'
          githublink="https://github.com/johnsonzhang434/portfolio"
          demolink='https://jzhang-portfolio.web.app/'
          cardimage='p4.png'
          cardcontent="A place where I can showcase my web development skills and experiences :)."

          :cardlanguages=" [
                          {
                            name: 'Vue',
                          },
                          {
                            name: 'Firebase',
                          },
                          {
                            name: 'Buefy',
                          },
                          {
                            name: 'SCSS',
                          }
                          ]"></Card>
      <!-- Project 1 -->
    <Card cardtitle='ACNH Field Guide'
          githublink='https://github.com/johnsonzhang434/ACNH-FieldGuide'
          demolink='https://anch-fieldguide.web.app/'
          cardimage='acnh.png'
          cardcontent="A full-stack web application that utilizes the public Animal Crossing API to keep track
of what animals users have caught."

          :cardlanguages=" [
                          {
                            name: 'Vue',
                          },
                          {
                            name: 'Firebase',
                          },
                          {
                            name: 'Tailwind',
                          },
                          {
                            name: 'JavaScript',
                            image: ''
                          },
                          {
                            name: 'HTML/CSS',
                            image: ''
                          }
                          ]"></Card>
    <!-- Project 2  -->
    <Card cardtitle='Airline Web Application'
          githublink='https://github.com/johnsonzhang434/AirlineWebApplication'
          cardimage='p2.jpeg'
          cardcontent="A full stack web application that
allows users to query, delete, add, and update flight information for airports in Canada."
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
                          },
                          {
                            name: 'HTML/CSS',
                            image: ''
                          }
                          ]"></Card>
      <!-- Project 3 -->
      <Card cardtitle='Visual Status Display'
            githublink='https://github.com/johnsonzhang434/VisualStatusDisplay'
            cardimage='p1.jpeg'
            cardcontent="A full stack web application to display a user's status
            to everyone in the local area. Their status is also displayed on a physical
            display mounted on their door."
            :cardlanguages=" [
                            {
                              name: 'TypeScript',
                              image: ''
                            },
                            {
                              name: 'JavaScript',
                              image: ''
                            },
                            {
                              name: 'HTML/CSS',
                              image: ''
                            }
                            ]"></Card> 
      <!-- Project 4 -->
      <Card cardtitle='SeetGeek.'
            githublink='https://github.com/johnsonzhang434/SeetGeek'
            cardimage='p3.jpeg'
            cardcontent="A full stack web application for a ticket-selling
                        system based on the popular application SeatGeek which
                        allows users to buy, sell and update tickets. Automated whitebox
                        and blockbox testing was done to ensure quality."
            :cardlanguages=" [
                            {
                              name: 'Flask',
                              image: ''
                            },
                            {
                              name: 'Selenium',
                              image: ''
                            },
                            {
                              name: 'SQLAlchemy',
                              image: ''
                            }
                            ]"></Card>     

                            <!-- Project 5 -->
      <Card cardtitle='My Previous Personal Website'
            githublink='https://johnsonzhang434.github.io/'
            cardimage='p5.png'
            cardcontent="An old place where I can showcase my web development skills and experiences :)."
            :cardlanguages=" [
                            {
                              name: 'JavaScript',
                              image: ''
                            },
                            {
                              name: 'HTML/CSS',
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
    .from(".card", { y : outerWidth * 0.2})
    }
  },
}
</script>
