<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isNavCollapsed: true,
      scrolled: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 50
    },
    toggleNav() {
      this.isNavCollapsed = !this.isNavCollapsed
    },
    closeNav() {
      this.isNavCollapsed = true
    }
  }
}
</script>

<template>
  <nav 
    class="navbar navbar-expand-lg fixed-top transition-all"
    :class="{ 'glass py-2': scrolled, 'bg-transparent py-4': !scrolled }"
  >
    <div class="container">
      <a class="navbar-brand fw-bold fs-3 d-flex align-items-center gap-2" href="#">
        <i class="fa-solid fa-code text-primary"></i>
        <span>Dev<span class="text-primary">Portfolio</span></span>
      </a>
      
      <button 
        class="navbar-toggler border-0 text-white" 
        type="button" 
        @click="toggleNav"
      >
        <i class="fa-solid fa-bars-staggered fs-3"></i>
      </button>

      <div 
        class="collapse navbar-collapse" 
        :class="{ 'show': !isNavCollapsed }"
      >
        <ul class="navbar-nav ms-auto align-items-center gap-lg-4">
          <li class="nav-item" v-for="(item, index) in ['Home', 'About', 'Services', 'Skills', 'Projects']" :key="index">
            <a 
              class="nav-link fw-medium" 
              :href="`#${item.toLowerCase()}`" 
              @click="closeNav"
            >
              {{ item }}
            </a>
          </li>
          <li class="nav-item ms-lg-2">
            <a href="#contact" class="btn btn-primary btn-sm px-4" @click="closeNav">
              Let's Talk <i class="fa-solid fa-arrow-right ms-2"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.transition-all {
  transition: all 0.4s ease;
}

.navbar-brand {
  color: #fff !important;
  font-family: 'Outfit', sans-serif;
}

.nav-link {
  color: #cbd5e1 !important;
  transition: color 0.3s ease;
  font-size: 0.95rem;
}

.nav-link:hover {
  color: #fff !important;
  text-shadow: 0 0 10px rgba(255,255,255,0.3);
}

@media (max-width: 991px) {
  .navbar-collapse {
    background: rgba(15, 23, 42, 0.98);
    backdrop-filter: blur(20px);
    padding: 2rem;
    border-radius: 1rem;
    margin-top: 1rem;
    box-shadow: 0 10px 50px rgba(0,0,0,0.5);
  }
}
</style>
