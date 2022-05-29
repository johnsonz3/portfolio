<template>
    <section style="height: 32rem;">
        <div class="about-header-background">
            <div class="profilePic">
                <img src="/images/profilepic2022.jpg"/>
            </div>
            <div class = "profileSocials">
                <div class="introduction">
                    <span class="introduction-title">
                        Hi I'm Johnson!
                    </span><br><br>
                    <span style="font-size: 1.2rem; color: #e1ccf9;"> 
                        I recently graduated from Queen's University CS with a specialization in software design.
                    </span>
                </div>
                <div class="about-links">
                    <a href="https://www.linkedin.com/in/johnsonzhang2/" target="blank">
                        LinkedIn
                    </a>
                    <a href="https://github.com/johnsonzhang434" target="blank">
                        Github
                    </a>
                    <a href="/Johnsons-Resume.pdf" target="blank">
                        Resume
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>
<style>
    .introduction-title {
        font-size: 2rem; 
        font-weight: bold; 
        color: #cfc5e9;
    }
</style>
<script>

export default ({
    name: 'aboutHeader',
})
</script>
