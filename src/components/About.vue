<script>
export default {
  name: 'About',
  data() {
    return {
      stats: [
        { label: 'Years Experience', value: '5+' },
        { label: 'Projects Completed', value: '50+' },
        { label: 'Happy Clients', value: '30+' }
      ]
    }
  }
}
</script>

<template>
  <section id="about" class="py-5">
    <div class="container">
      <div class="row align-items-center gx-5">
        <div class="col-lg-6 mb-5 mb-lg-0">
          <div class="position-relative">
            <div class="image-wrapper glass-card p-2">
              <img src="https://placehold.co/600x600/1e293b/FFFFFF?text=About+Me" alt="About Me" class="img-fluid rounded shadow-lg w-100">
            </div>
            <!-- Floating Badge -->
            <div class="floating-badge glass p-3 rounded d-flex align-items-center gap-3">
              <div class="icon-box bg-primary text-white rounded-circle d-flex align-items-center justify-content-center" style="width: 50px; height: 50px;">
                <span class="fs-4">🚀</span>
              </div>
              <div>
                <h6 class="m-0 fw-bold">Fast Learner</h6>
                <small class="text-secondary">Always Evolving</small>
              </div>
            </div>
          </div>
        </div>
        
        <div class="col-lg-6">
          <h2 class="section-title text-start mx-0">About Me</h2>
          <h3 class="fw-bold mb-4">Crafting digital experiences with passion and precision.</h3>
          <p class="text-secondary mb-4">
            I am a dedicated Full Stack Developer with a passion for creating seamless user experiences. 
            My journey in web development started with a curiosity for how things work, and it has evolved into a career 
            where I solve complex problems with clean, efficient code.
          </p>
          <p class="text-secondary mb-5">
            When I'm not coding, you can find me exploring new technologies, contributing to open source, or enjoying a good cup of coffee.
          </p>
          
          <div class="row g-4">
            <div class="col-sm-4" v-for="(stat, index) in stats" :key="index">
              <div class="glass-card p-3 text-center">
                <h2 class="fw-bold text-gradient mb-1">{{ stat.value }}</h2>
                <small class="text-secondary">{{ stat.label }}</small>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.floating-badge {
  position: absolute;
  bottom: 30px;
  right: -20px;
  max-width: 250px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
}

@media (max-width: 991px) {
  .floating-badge {
    right: 0;
    bottom: -20px;
  }
}
</style>
