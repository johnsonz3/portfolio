<template>
  <div class="column">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title has-text-grey">
          Animal Crossing Field Guide
        </p>
      </header>
      <div class="card-content">
        <div class="content has-text-centered">
          <b-icon
            :icon="icon"
            size="is-large"
            type="is-primary"
          />
        </div>
      </div>
      <footer class="card-footer">
        <p class="card-footer-title has-text-grey">
        </p>
        <div class="card-footer-item">
          <span>
            Java
          </span>
        </div>
        <div class="card-footer-item">
          <span>
            Java
          </span>
        </div>
        <div class="card-footer-item">
          <span>
            Java
          </span>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BuefyCard',
  props: {
    title: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: true
    }
  }
}
</script>
