<template>
    <section>
        <div class="page-title"><h2>Top Skills</h2></div>
        <ProgressBar title="Python" :percentage="95" color="steelblue" :width="14"/>
        <ProgressBar title="Java" :percentage="90" color="maroon" :width="14"/>
        <ProgressBar title="ClojureScript" :percentage="80" color="mediumslateblue" :width="14"/>
        <ProgressBar title="VueJS" :percentage="85" color="mediumseagreen" :width="14"/>
        <ProgressBar title="ReactJS" :percentage="60" color="cornflowerblue" :width="14"/>
        <ProgressBar title="SQL" :percentage="80" color="purple" :width="14"/>
    </section>
</template>

<script>
import ProgressBar from '../components/ProgressBar.vue'

export default {
    name: 'skillsList',
    components: {
        ProgressBar
  },
  options: {
    text: {
        color: '#FFFFFF',
        shadowEnable: true,
        shadowColor: '#000000',
        fontSize: 14,
        fontFamily: 'Helvetica',
        dynamicPosition: false,
        hideText: false
    },
    progress: {
        color: '#2dbd2d',
        backgroundColor: '#C0C0C0'
    },
    layout: {
        height: 35,
        width: 140,
        verticalTextAlign: 61,
        horizontalTextAlign: 43,
        zeroOffset: 0,
        strokeWidth: 30,
        progressPadding: 0,
        type: 'line'
    }
  }
}
</script>