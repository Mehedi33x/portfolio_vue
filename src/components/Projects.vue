<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        { 
          title: 'E-Commerce Store', 
          category: 'Web Application',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=E-Store' 
        },
        { 
          title: 'Portfolio Design', 
          category: 'UI/UX Design',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=Portfolio' 
        },
        { 
          title: 'Task Manager', 
          category: 'Productivity',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=Task+App' 
        },
         { 
          title: 'Dashboard UI', 
          category: 'Frontend',
          image: 'https://placehold.co/600x400/1e293b/FFFFFF?text=Dashboard' 
        }
      ]
    }
  }
}
</script>

<template>
  <section id="projects" class="py-5 bg-darker">
    <div class="container">
      <h2 class="section-title">Featured Projects</h2>
      
      <div class="row g-4">
        <div class="col-md-6 col-lg-3" v-for="(project, index) in projects" :key="index">
          <div class="project-card glass-card overflow-hidden h-100 group">
            <div class="position-relative overflow-hidden project-img-wrapper">
              <img :src="project.image" :alt="project.title" class="img-fluid w-100 project-img">
              <div class="overlay d-flex align-items-center justify-content-center">
                <button class="btn btn-light btn-sm rounded-circle px-3 py-2">View</button>
              </div>
            </div>
            <div class="p-4">
              <small class="text-primary text-uppercase fw-bold">{{ project.category }}</small>
              <h5 class="mt-2 mb-0 fw-bold">{{ project.title }}</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.project-card {
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.project-img-wrapper {
  position: relative;
}

.project-img {
  transition: transform 0.5s ease;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(15, 23, 42, 0.8);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .overlay {
  opacity: 1;
}

.project-card:hover .project-img {
  transform: scale(1.1);
}
</style>
