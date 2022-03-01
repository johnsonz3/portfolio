<template>
<div>
    <section style="width: 100%; height: 100vh;">
        <div v-if="window.width >= 800" class="item">
            <AboutHeader/>
        </div>
        <div v-else class="item">
            <AboutHeaderAlt/>
        </div>
        
        <div class="about-container">
            <!-- I have recently found a passion for full stack development. This passion came from my previous relevant experiences. The feeling of having a web application, that I built, deployed, is one of the best feelings ever! -->
        </div>
    </section>
    <section>
    </section>
    <section>
    </section>
</div>
</template>
<script>
import AboutHeader from '../layouts/aboutHeader.vue';
import AboutHeaderAlt from '../layouts/aboutHeaderAlt.vue';

export default ({
    name: 'AboutLayout',
    components: {
        AboutHeader,
        AboutHeaderAlt
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
})
</script>
