<template>
    <div class="card">
      <div class="card-image">
        <figure class="image is-4by3">
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
          <ul>
            <li v-for="item in cardlanguages" :key="item.name">
              {{ item.name }}
            </li>
          </ul>     
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
    cardlanguages: Array
      }
 
}
</script>
