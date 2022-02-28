<template>
  <div :style="'position:relative;width:'+ width +'rem;'" class="progress-skill-container">
      <div style="margin-left: 1rem; vertical-align:middle; line-height: 1.5rem; width:10rem;">
        <span class="progress-label-title">{{title}}</span>
      </div>
      <div @mouseover="display = 'Block'" @mouseleave="display = 'None'" class="progress-skill-bar-container" style="width:50%;">
        <div :style="progressBarStyle" class="progress-skill-bar">
          <div class="percentage-title">
            {{percentage}}%
          </div>
        </div>
        <div class="progress-skill-bar-background"></div>
      </div>
  </div>
</template>
<script>
export default {
    name: 'ProgressBar',
    props: {
        color: String,
        width: Number,
        percentage: Number,
        title: String,
        language: String
    },
   computed: {
    progressBarStyle() {
      return {
        "background-color": this.color,
        "width": this.percentage+"%",
        "animation": "slide 1s",
        "animation-duration": "1s",
        "--from-width":"0",
        "--to-width": this.percentage+"%"
      };
    }
  }
}
</script>