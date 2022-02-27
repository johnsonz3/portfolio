<template>
    <b-navbar shadow fixed-bottom is-spaced class="is-grey is-light">
        <template #brand>
               <div class="copyright">
                <img src="../static/icons/copyright.png">
                Johnson Zhang 2022 | New Grad Software Engineer
                </div>
        </template>
          <template #end>
           <b-navbar-item href="https://github.com/johnsonzhang434" target="_blank">
                 <img src="../static/icons/github-icon.png">
           </b-navbar-item>
           <b-navbar-item href="https://www.linkedin.com/in/johnson-zhang-ba77b1163/" target="_blank">
               <img src="https://img.icons8.com/ios-glyphs/30/000000/linkedin-2--v2.png"/>
           </b-navbar-item>
            
        </template>
    </b-navbar>
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
