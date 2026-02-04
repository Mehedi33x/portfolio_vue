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
    :class="{ 'glass navbar-dark py-2': scrolled, 'navbar-dark bg-transparent py-4': !scrolled }"
  >
    <div class="container">
      <a class="navbar-brand fw-bold fs-3" href="#">
        Portfolio<span class="text-primary-custom">.</span>
      </a>
      
      <button 
        class="navbar-toggler border-0" 
        type="button" 
        @click="toggleNav"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div 
        class="collapse navbar-collapse" 
        :class="{ 'show': !isNavCollapsed }"
      >
        <ul class="navbar-nav ms-auto align-items-center">
          <li class="nav-item" v-for="item in ['Home', 'About', 'Services', 'Skills', 'Projects', 'Contact']" :key="item">
            <a 
              class="nav-link px-3 fw-medium" 
              :href="`#${item.toLowerCase()}`" 
              @click="closeNav"
            >
              {{ item }}
            </a>
          </li>
          <li class="nav-item ms-lg-3 mt-3 mt-lg-0">
            <a href="#contact" class="btn btn-primary btn-sm px-4" @click="closeNav">Hire Me</a>
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
  letter-spacing: -1px;
}

.text-primary-custom {
  color: var(--secondary-color);
}

.nav-link {
  color: rgba(255, 255, 255, 0.8) !important;
  position: relative;
}

.nav-link:hover, .nav-link.active {
  color: #fff !important;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0px;
  left: 50%;
  width: 0;
  height: 2px;
  background: var(--secondary-color);
  transition: all 0.3s ease;
  transform: translateX(-50%);
}

.nav-link:hover::after {
  width: 80%;
}

/* Mobile Menu Glass override */
@media (max-width: 991px) {
  .navbar-collapse {
    background: rgba(15, 23, 42, 0.95);
    backdrop-filter: blur(10px);
    padding: 1rem;
    border-radius: 1rem;
    margin-top: 1rem;
    border: 1px solid rgba(255,255,255,0.1);
  }
}
</style>
