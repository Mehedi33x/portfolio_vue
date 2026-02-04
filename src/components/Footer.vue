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
  <footer class="py-4 text-center border-top border-white border-opacity-10 position-relative z-1">
    <div class="container">
      <p class="mb-0 text-secondary">
        &copy; {{ year }} DevPortfolio. Built with <i class="fa-solid fa-heart text-danger animate__animated animate__pulse animate__infinite"></i> using Vue.js & Bootstrap.
      </p>
    </div>
  </footer>
</template>
