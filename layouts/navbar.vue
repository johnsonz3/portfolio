<template>
    <b-navbar shadow centered >
        <template #brand>
           <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <span class="web-title"> Johnson Zhang </span>
            </b-navbar-item>
        </template>
        
          <template #start>
              <b-navbar-item tag="router-link" :to="{ path: '/' }">
                  Home
              </b-navbar-item>
              <b-navbar-item tag="router-link" :to="{ path: '/Project' }">
                  Projects
              </b-navbar-item>
            
              <b-navbar-item tag="router-link" :to="{ path: '/About' }">
                  About
              </b-navbar-item>
              <b-navbar-item href="#">
                  Contact
              </b-navbar-item>
              <b-navbar-item href="#">
                  Resume
              </b-navbar-item>
              <b-navbar-item >
                 <i class="fal fa-sun"></i>
              </b-navbar-item>
          </template>

          <template #end>
           <div class="empty-space">
           </div>
        </template>
    </b-navbar>
</template>
<script>
export default {
  name: 'NavbarLayout',
  data () {
    return {
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
