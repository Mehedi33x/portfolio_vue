<script>
export default {
  name: 'Footer',
  data() {
    return {
      year: new Date().getFullYear()
    }
  }
}
</script>

<template>
  <footer class="py-4 text-center glass border-top-0">
    <div class="container">
      <p class="mb-0 text-secondary">
        &copy; {{ year }} MyPortfolio. All rights reserved. 
        <span class="d-block d-md-inline mt-2 mt-md-0 ms-md-2">Designed with ❤️ in Vue.js</span>
      </p>
    </div>
  </footer>
</template>

<style scoped>
</style>
