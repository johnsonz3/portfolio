<template>
    <div class="footerSection">
      <div class="copyright">
        <img src="../static/icons/copyright.png">
        Johnson Zhang 2022 | New Grad Software Engineer
      </div>
      <div class="socials">
        <a href="https://github.com/johnsonzhang434" target="blank">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'github' }" class="icon-github"/>
        </a>
        <a href="https://www.linkedin.com/in/johnsonzhang2/" target="blank">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'linkedin-in' }" class="icon-github"/>
        </a>
      </div>
    </div>       
</template>

<script>
export default {
  name: 'footerSec',
  data () {
    return {
      publicPath: process.env.BASE_URL,
    }
  }
}
</script>
