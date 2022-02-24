<template>
    <b-navbar class="navbar">
        <template #brand>
            <b-navbar-item class="web-title" tag="router-link" :to="{ path: '/' }">
                Johnson Zhang
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-item href="#">
                Home
            </b-navbar-item>
            <b-navbar-item href="#">
                Projects
            </b-navbar-item>
            <b-navbar-dropdown label="Info">
                <b-navbar-item href="#">
                    About
                </b-navbar-item>
                <b-navbar-item href="#">
                    Contact
                </b-navbar-item>
                <b-navbar-item href="#">
                    Resume
                </b-navbar-item>
            </b-navbar-dropdown>
        </template>

       
    </b-navbar>
</template>

<style scoped>
.navbar{
  border-bottom: 2px solid grey;
}
.web-title {
  font-size: 1.3rem;
  color:blueviolet;
}
.web-title:hover {
  color:blueviolet;
}
</style>
<script>
export default {
  name: 'DefaultLayout',
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
