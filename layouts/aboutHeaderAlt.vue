<template>
    <section style="height: 42rem;">
        <div class="about-header-backgroundAlt">
            <div class="profilePicAlt">
                <img src="/images/profilepic2022.jpg"/>
            </div>
        </div>
        <div class = "profileSocialsAlt">
                <div class="introductionAlt">
                    <span class="introduction-title">
                        Hi I'm Johnson!
                    </span><br><br>
                    <span style="font-size: 1.2rem; color: black;"> 
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
              <div style="border-bottom: 1px solid lightgrey; width: 80%; margin-left: 10%;"></div>
            </div>
    </section>
</template>
<style scoped>
    .introduction-title {
        font-size: 2rem; 
        font-weight: bold; 
        color: rgb(92, 78, 182);
    }
</style>
<script>

export default ({
    name: 'aboutHeader',
})
</script>
