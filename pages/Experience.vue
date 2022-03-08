<template>
    <section>
        <Navbar/>
        <experiencePage/>
        <FooterSection/>
    </section>
</template>
<script>
import Navbar from '../layouts/navbar.vue';
import FooterSection from '../layouts/FooterSection.vue';
import experiencePage from '../layouts/experiencePage.vue'
export default ({
    name: "experience",
    components: {
        Navbar,
        FooterSection,
        experiencePage
    }
})
</script>
