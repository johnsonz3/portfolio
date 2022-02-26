<template>
  <div class="skill-card">
  <div class="skill-div">
  <vue-ellipse-progress 
  :progress=percentage
  :color=color
  emptyColor="lightgrey"
  :size="200"
  thickness="10%"
  emptyThickness="9%"
  lineMode="normal 10"
  :legend="true"
  :loading="false"                      
  :fontColor=color
  fontSize="1.4rem"
  :gap="10">
  <span slot="legend-value">%</span>
    </vue-ellipse-progress>
  </div>
  <div class="skill-label">
    <div class="icon"><img :src="'/languages/' + language"/></div>
    <div><span class="skill-label-title">{{title}}</span></div>
  </div>
  </div>
</template>
<script>
export default {
    name: 'Skill',
    props: {
        color: String,
        percentage: Number,
        title: String,
        language: String
    },
   
}
</script>