<script>
export default {
  name: 'Home',
  data() {
    return {
      title: "Creative Developer",
      subtitle: "I build exceptional digital experiences."
    }
  }
}
</script>

<template>
  <section id="home" class="min-vh-100 d-flex align-items-center position-relative overflow-hidden">
    <!-- Background Elements -->
    <div class="bg-blur-1"></div>
    <div class="bg-blur-2"></div>

    <div class="container position-relative z-1">
      <div class="row align-items-center">
        <div class="col-lg-7 text-center text-lg-start">
          <span class="badge rounded-pill bg-light text-dark px-3 py-2 mb-4 fw-bold">👋 Welcome to my portfolio</span>
          <h1 class="display-1 fw-bold mb-4 lh-1">
            <span class="text-gradient">{{ title }}</span>
          </h1>
          <p class="lead text-secondary mb-5 fs-4" style="max-width: 600px;">
            {{ subtitle }} Transforming ideas into interactive reality with modern web technologies.
          </p>
          <div class="d-flex gap-3 justify-content-center justify-content-lg-start">
            <a href="#projects" class="btn btn-primary btn-lg">View Work</a>
            <a href="#contact" class="btn btn-outline-light btn-lg">Contact Me</a>
          </div>
        </div>
        
        <!-- Optional Hero Image/Graphic -->
        <div class="col-lg-5 d-none d-lg-block">
          <div class="hero-graphic glass-card p-4">
            <div class="code-block">
              <div class="d-flex gap-2 mb-3">
                <span class="dot bg-danger"></span>
                <span class="dot bg-warning"></span>
                <span class="dot bg-success"></span>
              </div>
              <pre class="m-0 text-success"><code>const developer = {
  name: 'You',
  skills: ['Vue', 'Design', 'Code'],
  passion: true,
  hireable: true
};</code></pre>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.bg-blur-1 {
  position: absolute;
  top: -10%;
  left: -10%;
  width: 50vw;
  height: 50vw;
  background: var(--primary-color);
  filter: blur(150px);
  opacity: 0.2;
  border-radius: 50%;
  z-index: 0;
}

.bg-blur-2 {
  position: absolute;
  bottom: -10%;
  right: -10%;
  width: 40vw;
  height: 40vw;
  background: var(--secondary-color);
  filter: blur(150px);
  opacity: 0.15;
  border-radius: 50%;
  z-index: 0;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.code-block {
  font-family: 'Fira Code', monospace;
  font-size: 0.9rem;
}
</style>
