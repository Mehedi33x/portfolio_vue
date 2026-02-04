<script>
export default {
  name: "Home",
  data() {
    return {
      badgeText: "Available for Freelance Work",

      heading: {
        line1: "Building Digital",
        highlight: "Masterpieces",
      },

      description:
        "I help brands simplify their user experience and scale their impact with modern, high-performance web applications.",

      buttons: {
        portfolio: {
          text: "View Portfolio",
          link: "#projects",
          icon: "fa-briefcase",
        },
        contact: {
          text: "Contact Me",
          link: "#contact",
          icon: "fa-envelope",
        },
      },

      socials: [
        { icon: "fa-github", link: "https://github.com/mehedi33x" },
        { icon: "fa-linkedin-in", link: "https://www.linkedin.com/in/mehedi-hasan-33x/" },
        // { icon: "fa-twitter", link: "#" },
        // { icon: "fa-instagram", link: "#" },
      ],

      codeCard: {
        file: "app.js",
        name: "Mehedi Hassan",
        role: "Full Stack",
        coffee: true,
        output: "Clean & Scalable",
      },
    };
  },
};
</script>

<template>
  <section id="home" class="min-vh-100 d-flex align-items-center position-relative overflow-hidden section-padding">
    <!-- Animated Background Blobs -->
    <div class="blob bg-primary rounded-circle"
      style="width: 500px; height: 500px; top: -10%; left: -10%; opacity: 0.2"></div>
    <div class="blob bg-secondary rounded-circle" style="
        width: 400px;
        height: 400px;
        bottom: 10%;
        right: -5%;
        opacity: 0.2;
        animation-delay: -5s;
      "></div>

    <div class="container position-relative z-1">
      <div class="row align-items-center">
        <!-- LEFT CONTENT -->
        <div class="col-lg-7 text-center text-lg-start mb-5 mb-lg-0">
          <div
            class="d-inline-flex align-items-center gap-2 px-3 py-2 rounded-pill glass border-0 mb-4 text-primary fw-medium animate__animated animate__fadeInDown">
            <i class="fa-solid fa-star"></i> {{ badgeText }}
          </div>

          <h1 class="display-2 fw-bold mb-4 animate__animated animate__fadeInUp">
            {{ heading.line1 }} <br />
            <span class="text-gradient">{{ heading.highlight }}</span>
          </h1>

          <p class="lead text-secondary mb-5 fs-5 animate__animated animate__fadeInUp animate__delay-1s"
            style="max-width: 600px">
            {{ description }}
          </p>

          <div
            class="d-flex gap-3 justify-content-center justify-content-lg-start animate__animated animate__fadeInUp animate__delay-1s">
            <a :href="buttons.portfolio.link" class="btn btn-primary btn-lg shadow-lg">
              <i class="fa-solid me-2" :class="buttons.portfolio.icon"></i>
              {{ buttons.portfolio.text }}
            </a>

            <a :href="buttons.contact.link" class="btn btn-primary btn-lg shadow-lg">
              <i class="fa-solid me-2" :class="buttons.contact.icon"></i>
              {{ buttons.contact.text }}
            </a>
          </div>

          <div
            class="mt-5 d-flex gap-4 justify-content-center justify-content-lg-start text-secondary animate__animated animate__fadeInUp animate__delay-2s">
            <a v-for="(social, index) in socials" :key="index" :href="social.link" target="_blank"
    rel="noopener noreferrer" class="fs-4 social-icon">
              <i class="fa-brands" :class="social.icon"></i>
            </a>
          </div>
        </div>

        <!-- RIGHT CODE CARD -->
        <div class="col-lg-5 d-none d-lg-block animate__animated animate__fadeInRight">
          <div class="position-relative">
            <div class="glass-card p-4 tilt-effect text-start">
              <div class="d-flex justify-content-between mb-4 border-bottom border-light border-opacity-10 pb-3">
                <div class="d-flex gap-2">
                  <div class="rounded-circle bg-danger" style="width: 12px; height: 12px"></div>
                  <div class="rounded-circle bg-warning" style="width: 12px; height: 12px"></div>
                  <div class="rounded-circle bg-success" style="width: 12px; height: 12px"></div>
                </div>
                <small class="text-secondary font-monospace">
                  {{ codeCard.file }}
                </small>
              </div>

              <pre class="m-0 font-monospace text-light small">
<span class="text-primary">class</span> Developer {
  <span class="text-info">constructor</span>() {
    <span class="text-warning">this</span>.name = <span class="text-success">'{{ codeCard.name }}'</span>;
    <span class="text-warning">this</span>.role = <span class="text-success">'{{ codeCard.role }}'</span>;
    <span class="text-warning">this</span>.coffee = <span class="text-primary">{{ codeCard.coffee }}</span>;
  }

  <span class="text-info">code</span>() {
    <span class="text-warning">return</span> <span class="text-success">"{{ codeCard.output }}"</span>;
  }
}
</pre>

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
