<template>
    <div class="card">
      <a :href="link" target="blank">
        <div class="card-image">
          <figure class="image is-6by3">
            <img v-bind:src="'/images/' + cardimage" :alt="cardimage">
          </figure>
        </div>
        <div class="card-content">
          <div class="media">
            <div class="media-content">
              <p class="title is-4">{{cardtitle}}</p>
            </div>
          </div>

          <div class="content">
            {{ cardcontent}}
            <div class="languages-container">
              <div v-for="item in cardlanguages" :key="item.name">
                <b-field>
                    <b-tag type="is-primary is-light" >#{{item.name}} </b-tag>
                </b-field>
              </div>
            </div>     
          </div>
        </div>
      </a>
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
    link: String
      }
 
}
</script>
