<template>
  <div>
    <div class="page-title"><h2>Projects</h2></div>
    <div class="card-container">
      <!-- Project 1 -->
    <Card cardtitle='ACNH Field Guide'
          link='https://anch-fieldguide.web.app/'
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
                          }
                          ]"></Card>
    <!-- Project 2  -->
    <Card cardtitle='Airline Web Application'
          link='https://github.com/johnsonzhang434/AirlineWebApplication'
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
                          }
                          ]"></Card>
      <!-- Project 3 -->
      <Card cardtitle='Visual Status Display.'
            link='https://github.com/johnsonzhang434/VisualStatusDisplay'
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
            link='https://github.com/johnsonzhang434/SeetGeek'
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
