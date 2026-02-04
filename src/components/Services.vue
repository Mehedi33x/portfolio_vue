<script>
export default {
  name: 'Services',
  data() {
    return {
      services: [
        { title: 'Web Development', desc: 'Building responsive and high-performance websites.', icon: '💻' },
        { title: 'UI/UX Design', desc: 'Creating intuitive and visual user interfaces.', icon: '🎨' },
        { title: 'Mobile Apps', desc: 'Developing cross-platform mobile applications.', icon: '📱' },
        { title: 'SEO Optimization', desc: 'Improving visibility and ranking on search engines.', icon: '🚀' }
      ]
    }
  }
}
</script>

<template>
  <section id="services" class="py-5 bg-darker">
    <div class="container">
      <div class="text-center">
        <h2 class="section-title">My Services</h2>
      </div>
      
      <div class="row g-4 pt-4">
        <div class="col-md-6 col-lg-3" v-for="(service, index) in services" :key="index">
          <div class="service-card glass-card p-4 h-100 text-center">
            <div class="icon-wrapper mb-4 mx-auto d-flex align-items-center justify-content-center text-white">
              <span class="display-5">{{ service.icon }}</span>
            </div>
            <h4 class="mb-3">{{ service.title }}</h4>
            <p class="text-secondary mb-0">{{ service.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.bg-darker {
  background-color: rgba(2, 6, 23, 0.5);
}

.icon-wrapper {
  width: 80px;
  height: 80px;
  background: var(--card-bg);
  border-radius: 50%;
  box-shadow: 0 0 20px rgba(108, 99, 255, 0.1);
  transition: all 0.3s ease;
}

.service-card:hover .icon-wrapper {
  background: var(--gradient-main);
  transform: scale(1.1);
}
</style>
