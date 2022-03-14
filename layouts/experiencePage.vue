<template>
    <div>
        <div class="page-title">Work <span style="color:blueviolet;">Experience</span></div>
        <div class="experience-container">
            <div class="experience-card">
                <div class="experience-description">
                    <div class="experience-card-header">
                        <div><span class="experience-card-title">Teaching Assistant • DBMS</span></div>
                        <div class="date">Jan. 2022 - <span style="font-style: italic">Present</span></div>
                    </div>
                    <div class="experience-card-company">
                        Queen's University School of Computing
                    </div>
                    <div style="padding-bottom: 1rem;">
                        Kingston, ON, Canada
                    </div>
                    <div class="experience-description">
                        <p>• Guide 30 students through new learning material and aid with understanding assignments
                        done in PHP, MySQL, JavaScript, HTML and CSS</p>
                        <p>• Provide feedback and foster an environment of open communication and curiosity</p>
                    </div>
                </div>
            </div>

            <div class="experience-card">
                <div class="experience-description">
                    <div class="experience-card-header">
                        <div><span class="experience-card-title">Software Engineer</span></div>
                        <div class="date">Dec. 2021 - Jan. 2022</div>
                    </div>
                    <div class="experience-card-company">
                        Cotton Candy Inc.
                    </div>
                    <div style="padding-bottom: 1rem;">
                        Mississauga, ON, Canada
                    </div>
                    <div class="experience-description">
                        <p>• Resolved issues and refactored 100+ lines of code which resulted in a more efficient and
                             polished system using JavaScript, Clojure/Clojurescript, HTML and CSS
                        </p>
                    </div>
                </div>
            </div>

            <div class="experience-card">
                <div class="experience-description">
                    <div class="experience-card-header">
                        <div><span class="experience-card-title">Frontend Engineer</span></div>
                        <div class="date">May 2021 - Aug. 2021</div>
                    </div>
                    <div class="experience-card-company">
                        Cotton Candy Inc.
                    </div>
                    <div style="padding-bottom: 1rem;">
                        Mississauga, ON, Canada
                    </div>
                    <div class="experience-description">
                        <p>• Developed a customization tool that allows users to easily design and purchase products
                            using Clojure/Clojurescript, JavaScript, Shopify Liquid, HTML and CSS
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
    .date {
        padding-top: 0.2rem;
        font-size: 1.2rem;
        font-weight: normal;
    }
    .experience-container {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 2rem 1rem 7rem 1rem;
        gap: 1.5rem;
    }
    .experience-card {
        display: flex;
        flex-direction: column;
        width: 100%;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    }
    .experience-card:hover{
        box-shadow: 0 10px 10px -4px rgb(204, 149, 255);
    }
    .experience-description {
        padding: 0.7rem;
    }
    .experience-card-header{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        font-size: 1.5rem;
        font-weight: bold;
    }
    .experience-card-title{
        color: rgb(168, 0, 219);
    }
    .experience-card-company {
        font-weight: bold;
    }
    .experience-description {
        font-size: 1rem;
    }
</style>
<script>
import gsap from 'gsap';
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default ({
    name: "experiencePage",
        mounted: function() {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
        gsap.timeline({
        scrollTrigger: {
            trigger: ".experience-card",
        }
        })
        .from(".experience-card", { y : outerWidth * 0.2})
        }
    },
})
</script>