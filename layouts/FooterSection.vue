<template>
    <section>
      <div class="footerSection">
        <div class="copyright">
          <img src="../static/icons/copyright.png">
          Johnson Zhang 2022 | New Grad Software Engineer
        </div>
        <div class="socials">
          <a href="https://github.com/johnsonzhang434" target="blank">
            <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'github' }" class="icon-github"/>
          </a>
          <a href="https://www.linkedin.com/in/johnson-zhang-ba77b1163/" target="blank">
            <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'linkedin-in' }" class="icon-github"/>
          </a>
        </div>
     </div>       
    </section>
</template>

<script>
export default {
  name: 'footerSec',
  data () {
    return {
      publicPath: process.env.BASE_URL,
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>
