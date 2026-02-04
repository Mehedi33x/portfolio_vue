<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        { name: 'PHP', icon: 'fa-php', color: '#777BB4', level: 90 },
        { name: 'Laravel', icon: 'fa-laravel', color: '#FF2D20', level: 90 },
        { name: 'JavaScript', icon: 'fa-js', color: '#F7DF1E', level: 90 },
        { name: 'Vue.js', icon: 'fa-vuejs', color: '#4FC08D', level: 85 },
        { name: 'React', icon: 'fa-react', color: '#61DAFB', level: 80 },
        { name: 'RESTful API', icon: 'fa-cloud', color: '#6c757d', level: 85 },
        { name: 'Git', icon: 'fa-git-alt', color: '#F1502F', level: 90 },
        { name: 'GitHub', icon: 'fa-github', color: '#181717', level: 90 }
      ]
    }
  }
}
</script>

<template>
  <section id="skills" class="py-5 position-relative">
    <div class="container">
      <h2 class="section-title text-center" data-heading="EXPERTISE">My Skills</h2>
      
      <div class="row justify-content-center">
        <div class="col-lg-10">
          <div class="glass-card p-5">
            <div class="row g-5">
              <div class="col-md-6" v-for="(skill, index) in skills" :key="index">
                <div class="skill-item">
                  <div class="d-flex justify-content-between align-items-center mb-2">
                    <div class="d-flex align-items-center gap-2">
                      <i class="fa-brands fs-4" :class="skill.icon" :style="{ color: skill.color }"></i>
                      <span class="fw-bold fs-5">{{ skill.name }}</span>
                    </div>
                    <span class="fw-bold text-primary">{{ skill.level }}%</span>
                  </div>
                  <div class="progress" style="height: 10px; background: rgba(255,255,255,0.05); border-radius: 10px; overflow: visible;">
                    <div 
                      class="progress-bar position-relative" 
                      role="progressbar" 
                      :style="{ width: skill.level + '%', background: skill.color }" 
                      :aria-valuenow="skill.level" 
                      aria-valuemin="0" 
                      aria-valuemax="100"
                    >
                      <div class="glow" :style="{ background: skill.color }"></div>
                    </div>
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
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.3);
}
.glow {
  position: absolute;
  right: 0;
  top: 50%;
  transform: translate(50%, -50%);
  width: 15px;
  height: 15px;
  border-radius: 50%;
  box-shadow: 0 0 15px 2px currentColor;
  opacity: 0.8;
}
</style>
