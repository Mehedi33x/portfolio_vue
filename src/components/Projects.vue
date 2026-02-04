<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        { 
          title: 'Crypto Dashboard', 
          category: 'Fintech App',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=Crypto+Dash',
          tags: ['Vue', 'API', 'Chart.js']
        },
        { 
          title: 'Modern E-Commerce', 
          category: 'Shopping Platform',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=E-Store',
          tags: ['React', 'Node', 'Stripe']
        },
        { 
          title: 'Task Master', 
          category: 'Productivity Tool',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=Task+App',
          tags: ['Vue', 'Firebase']
        },
         { 
          title: 'AI Image Gen', 
          category: 'SaaS Application',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=AI+Gen',
          tags: ['OpenAI', 'Next.js']
        }
      ]
    }
  }
}
</script>

<template>
  <section id="projects" class="py-5">
    <div class="container">
      <h2 class="section-title text-center" data-heading="PORTFOLIO">Recent Work</h2>
      
      <div class="row g-4">
        <div class="col-md-6 col-lg-6" v-for="(project, index) in projects" :key="index">
          <div class="project-card glass-card p-0 h-100 group">
            <div class="position-relative overflow-hidden project-img-wrapper">
              <img :src="project.image" :alt="project.title" class="img-fluid w-100 project-img">
              
              <!-- Hover Overlay -->
              <div class="overlay d-flex flex-column align-items-center justify-content-center gap-3">
                <h4 class="fw-bold mb-1">{{ project.title }}</h4>
                <p class="text-light opacity-75 small text-uppercase spacing-1">{{ project.category }}</p>
                <div class="d-flex gap-2">
                  <button class="btn btn-primary btn-sm rounded-pill px-3">
                    <i class="fa-solid fa-eye me-1"></i> Demo
                  </button>
                  <button class="btn btn-outline-light btn-sm rounded-pill px-3">
                    <i class="fa-brands fa-github me-1"></i> Code
                  </button>
                </div>
              </div>
            </div>
            
            <div class="p-4 d-flex justify-content-between align-items-center">
              <div>
                <h5 class="fw-bold mb-1">{{ project.title }}</h5>
                <small class="text-secondary">{{ project.category }}</small>
              </div>
              <div class="d-flex gap-1">
                <span v-for="tag in project.tags" :key="tag" class="badge bg-white bg-opacity-10 text-white fw-light border border-white border-opacity-10">
                  {{ tag }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.project-img-wrapper {
  height: 250px;
}
.project-img {
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}
.overlay {
  position: absolute;
  inset: 0;
  background: rgba(15, 23, 42, 0.9);
  opacity: 0;
  transition: all 0.4s ease;
  backdrop-filter: blur(4px);
  transform: translateY(20px);
}
.project-card:hover .overlay {
  opacity: 1;
  transform: translateY(0);
}
.project-card:hover .project-img {
  transform: scale(1.1);
}
</style>
