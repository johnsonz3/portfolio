<template>
<div>
    <section style="width: 100%; height: 100vh;">
        <div v-if="window.width >= 600" class="item">
            <AboutHeader/>
        </div>
        <div v-else class="item">
            <AboutHeaderAlt/>
        </div>
        
        <div class="about-container container">
            <div class="about-text-container">
                <div class ="about-text">
                    <div class="about-header">
                        About
                    </div>
                    I have recently found a passion for full stack development. This passion came from my previous relevant experiences. I absolutely love building web applications!
                    <div>
                    <a href="/project">
                        <b-button class="is-primary is-light" rounded size="normal">Check out my projects!</b-button>
                    </a>
                    </div>
                </div>
                </div>
        </div>
        <div class="ts-container container">
            <div class="about-text-container">
                <div class="about-header">
                    Tech Stack
                </div>
                <div class="cardInfos">
                    <CardInfos/>
                </div>
            </div>
        </div>
    </section>
    <section>
    </section>
    <section>
    </section>
</div>
</template>
<style scoped>
.about-text {
    display: flex;
    flex-direction: column;
    gap: 2rem;
}
.about-header{
    font-weight: bold;
    font-size: 2rem;
}
.container {
    width: 100%;
    text-align: center;
    display: flex;
    justify-content: center;
}
.about-container {
    height: 18rem;
}
.ts-container {
    height: 40rem;
}
.about-text-container{
    width: 80%;
    display: flex;
    flex-direction: column;
}
</style>
<script>
import AboutHeader from '../layouts/aboutHeader.vue';
import AboutHeaderAlt from '../layouts/aboutHeaderAlt.vue';
import CardInfos from '../layouts/CardInfos.vue';
import gsap from 'gsap';
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
export default ({
    name: 'AboutLayout',
    components: {
        AboutHeader,
        AboutHeaderAlt,
        CardInfos
    },
    data () {
    return{
        window: {
            width: 0,
            height: 0
        }
    }
    },
    mounted() {
        this.scrollAnimation();
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
        },
        scrollAnimation() {
        gsap.timeline({
        scrollTrigger: {
            trigger: ".cardInfos",
        }
        })
        .from(".cardInfos", { y : outerWidth * 0.2})
        }
    },
       
})
</script>
