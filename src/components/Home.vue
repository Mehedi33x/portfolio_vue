<script>
export default {
  name: 'Home',
  data() {
    return {
      title: "Senior Full Stack Developer",
    }
  }
}
</script>

<template>
  <section id="home" class="min-vh-100 d-flex align-items-center position-relative overflow-hidden section-padding">
    <!-- Animated Background Blobs -->
    <div class="blob bg-primary rounded-circle" style="width: 500px; height: 500px; top: -10%; left: -10%; opacity: 0.2"></div>
    <div class="blob bg-secondary rounded-circle" style="width: 400px; height: 400px; bottom: 10%; right: -5%; opacity: 0.2; animation-delay: -5s"></div>

    <div class="container position-relative z-1">
      <div class="row align-items-center">
        <div class="col-lg-7 text-center text-lg-start mb-5 mb-lg-0">
          <div class="d-inline-flex align-items-center gap-2 px-3 py-2 rounded-pill glass border-0 mb-4 text-primary fw-medium animate__animated animate__fadeInDown">
            <i class="fa-solid fa-star"></i> Available for Freelance Work
          </div>
          
          <h1 class="display-2 fw-bold mb-4 animate__animated animate__fadeInUp">
            Building Digital <br>
            <span class="text-gradient">Masterpieces</span>
          </h1>
          
          <p class="lead text-secondary mb-5 fs-5 animate__animated animate__fadeInUp animate__delay-1s" style="max-width: 600px;">
            I help brands simplify their user experience and scale their impact with modern, high-performance web applications.
          </p>
          
          <div class="d-flex gap-3 justify-content-center justify-content-lg-start animate__animated animate__fadeInUp animate__delay-1s">
            <a href="#projects" class="btn btn-primary btn-lg shadow-lg">
              <i class="fa-solid fa-briefcase me-2"></i> View Portfolio
            </a>
            <a href="#contact" class="btn btn-outline-light btn-lg px-4">
              <i class="fa-solid fa-envelope me-2"></i> Contact Me
            </a>
          </div>

          <div class="mt-5 d-flex gap-4 justify-content-center justify-content-lg-start text-secondary animate__animated animate__fadeInUp animate__delay-2s">
            <a href="#" class="fs-4 social-icon"><i class="fa-brands fa-github"></i></a>
            <a href="#" class="fs-4 social-icon"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#" class="fs-4 social-icon"><i class="fa-brands fa-twitter"></i></a>
            <a href="#" class="fs-4 social-icon"><i class="fa-brands fa-instagram"></i></a>
          </div>
        </div>
        
        <div class="col-lg-5 d-none d-lg-block animate__animated animate__fadeInRight">
          <div class="position-relative">
            <div class="glass-card p-4 tilt-effect text-start">
              <div class="d-flex justify-content-between mb-4 border-bottom border-light border-opacity-10 pb-3">
                <div class="d-flex gap-2">
                  <div class="rounded-circle bg-danger" style="width: 12px; height: 12px"></div>
                  <div class="rounded-circle bg-warning" style="width: 12px; height: 12px"></div>
                  <div class="rounded-circle bg-success" style="width: 12px; height: 12px"></div>
                </div>
                <small class="text-secondary font-monospace">app.js</small>
              </div>
              <pre class="m-0 font-monospace text-light small">
<span class="text-primary">class</span> Developer {
  <span class="text-info">constructor</span>() {
    <span class="text-warning">this</span>.name = <span class="text-success">'Alex'</span>;
    <span class="text-warning">this</span>.role = <span class="text-success">'Full Stack'</span>;
    <span class="text-warning">this</span>.coffee = <span class="text-primary">true</span>;
  }

  <span class="text-info">code</span>() {
    <span class="text-warning">return</span> <span class="text-success">"Clean & Scalable"</span>;
  }
}</pre>
            </div>
            <!-- Floating element -->
            <div class="glass px-4 py-3 rounded-4 position-absolute shadow-lg d-flex gap-3 align-items-center" style="bottom: -20px; left: -20px;">
               <div class="bg-success rounded-circle p-2 text-white">
                 <i class="fa-solid fa-check"></i>
               </div>
               <div>
                 <h6 class="m-0 fw-bold">100% Success</h6>
                 <small class="text-secondary">Job Rating</small>
               </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.social-icon {
  color: var(--text-secondary);
  transition: all 0.3s ease;
}
.social-icon:hover {
  color: var(--primary-color);
  transform: translateY(-3px);
}
.tilt-effect {
  transform: perspective(1000px) rotateY(-5deg) rotateX(5deg);
  transition: transform 0.5s ease;
}
.tilt-effect:hover {
  transform: perspective(1000px) rotateY(0) rotateX(0);
}
</style>
