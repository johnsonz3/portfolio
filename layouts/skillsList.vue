<template>
    <section>
        <div class="page-title"><h2>Top Skills</h2></div>
            <div class="skills-page">
            <Skill v-bind:percentage=80 color="purple" title="SQL" language="sql.png"/>
            <Skill v-bind:percentage=80 color="mediumslateblue" title="ClojureScript" language="clojure.png"/>
            <Skill v-bind:percentage=85 color="mediumseagreen" title="VueJS" language="vue.png"/>
            <Skill v-bind:percentage=60 color="cornflowerblue" title="ReactJS" language="react.png"/>
       <Skill v-bind:percentage=95 color="steelblue" title="Python" language="python.png"/>
            <Skill v-bind:percentage=90 color="maroon" title="Java" language="java.png"/>
        </div>
    </section>
</template>

<script>
import Skill from '../components/Skill.vue'

export default {
    name: 'skillsList',
    components: {
        Skill
  }
}
</script>