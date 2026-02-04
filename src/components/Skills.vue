<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        { name: 'HTML/CSS', level: 95 },
        { name: 'JavaScript', level: 90 },
        { name: 'Vue.js', level: 85 },
        { name: 'Node.js', level: 80 },
        { name: 'Bootstrap', level: 90 },
        { name: 'Git/GitHub', level: 85 }
      ]
    }
  }
}
</script>

<template>
  <section id="skills" class="py-5">
    <div class="container">
      <h2 class="section-title">Professional Skills</h2>
      
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="glass-card p-5">
            <div class="row g-4">
              <div class="col-md-6" v-for="(skill, index) in skills" :key="index">
                <div class="skill-item">
                  <div class="d-flex justify-content-between mb-2">
                    <span class="fw-bold">{{ skill.name }}</span>
                    <span class="text-primary">{{ skill.level }}%</span>
                  </div>
                  <div class="progress" style="height: 10px; background: rgba(255,255,255,0.1);">
                    <div 
                      class="progress-bar progress-gradient" 
                      role="progressbar" 
                      :style="{ width: skill.level + '%' }" 
                      :aria-valuenow="skill.level" 
                      aria-valuemin="0" 
                      aria-valuemax="100"
                    ></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.progress-bar {
  border-radius: 5px;
  background: var(--gradient-main);
  box-shadow: 0 0 10px rgba(108, 99, 255, 0.5);
  transition: width 1.5s ease-in-out;
}
</style>
