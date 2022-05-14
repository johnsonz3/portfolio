<template>
    <section>
        <div class="main-page">
            <div class="text-container">
                <vue-typed-js :typeSpeed="100" :backSpeed="100" :smartBackspace="true" :backDelay="100" :strings="['Web Developer', 'Software Developer', 'Software Engineer']">
                <h1>Hello, my name is Johnson Zhang <span class="main-page-content-title"><br/>New Grad <span class="typing"></span><br/></span>
                <span style="font-size:1.2rem; color:grey;">
                Graduated in April, 2022
                </span></h1>
                </vue-typed-js>
                <div style="margin-top: 2rem;">
                    <a href="/experience">
                        <b-button class="is-primary is-light" rounded size="normal">Check out my Experiences</b-button>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>
<script>

export default ({
    name: 'IndexLayout',
})
</script>
