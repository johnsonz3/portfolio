<template>
    <div class="card">
        <div class="card-image">
          <figure class="image is-6by3">
            <img v-bind:src="'/images/' + cardimage" :alt="cardimage">
          </figure>
        </div>
        <div class="card-content">
          <div style="display: flex;">
            <p class="title is-4">{{cardtitle}}</p>
            <div style="margin-left:auto;">
              <a v-if="demolink" :href="demolink" target="blank">
                <b-button class="is-primary is-light" rounded size="is-small">Try it out</b-button>
              </a>
            </div>
          </div>

          <div class="content">
            {{ cardcontent}}
            <div class="languages-container">
              <div style="margin-right: 0.4rem;">
              Stack: 
              </div>
              <div v-for="item in cardlanguages" class="cardlanguages" :key="item.name">
                {{item.name}}
              </div>
            </div>     
            <div class="content">
              <b-field>
                <div style="display:flex; gap: 1rem;">
                  <a v-if="githublink" :href="githublink" target="blank">
                    <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'github' }" class="icon-github"/>
                  </a>
                </div>
              </b-field>
            </div>
          </div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'BuefyCard',
  props: {
    cardtitle: String,
    cardimage: String,
    cardcontent: String,
    cardlanguages: Array,
    githublink: String,
    demolink: String
      }
 
}
</script>
