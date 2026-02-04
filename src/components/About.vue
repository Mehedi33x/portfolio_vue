<script>
export default {
  name: 'About',
  data() {
    return {
      image: {
        src: "/frontend/images/image2.png",
        alt: "About Me",
      },

      floatingBadge: {
        emoji: "🚀",
        title: "Fast Learner",
        subtitle: "Always Evolving",
      },

      section: {
        title: "About Me",
        headline: "Crafting digital experiences with passion and precision.",
      },

      paragraphs: [
        "I am a dedicated Full Stack Developer with a passion for creating seamless user experiences. My journey in web development started with a curiosity for how things work, and it has evolved into a career where I solve complex problems with clean, efficient code.",
        "When I'm not coding, you can find me exploring new technologies, contributing to open source, or enjoying a good cup of coffee.",
      ],

      stats: [
        { label: "Years Experience", value: "2+" },
        { label: "Projects Completed", value: "10+" },
        { label: "Happy Clients", value: "5+" },
      ],
    }
  },
}
</script>

<template>
  <section id="about" class="py-5">
    <div class="container">
      <div class="row align-items-center gx-5">
        <!-- IMAGE SIDE -->
        <div class="col-lg-6 mb-5 mb-lg-0">
          <div class="position-relative">
            <div class="image-wrapper glass-card p-2">
              <img :src="image.src" :alt="image.alt" class="img-fluid rounded shadow-lg w-100" />
            </div>

            <!-- Floating Badge -->
            <div class="floating-badge glass p-3 rounded d-flex align-items-center gap-3">
              <div
                class="icon-box bg-primary text-white rounded-circle d-flex align-items-center justify-content-center"
                style="width: 50px; height: 50px">
                <span class="fs-4">{{ floatingBadge.emoji }}</span>
              </div>
              <div>
                <h6 class="m-0 fw-bold">{{ floatingBadge.title }}</h6>
                <small class="text-secondary">
                  {{ floatingBadge.subtitle }}
                </small>
              </div>
            </div>
          </div>
        </div>

        <!-- CONTENT SIDE -->
        <div class="col-lg-6">
          <h2 class="section-title text-start mx-0">
            {{ section.title }}
          </h2>

          <h3 class="fw-bold mb-4">
            {{ section.headline }}
          </h3>

          <p v-for="(text, index) in paragraphs" :key="index" class="text-secondary mb-4">
            {{ text }}
          </p>

          <div class="row g-4">
            <div class="col-sm-4" v-for="(stat, index) in stats" :key="index">
              <div class="glass-card p-3 text-center">
                <h2 class="fw-bold text-gradient mb-1">
                  {{ stat.value }}
                </h2>
                <small class="text-secondary">
                  {{ stat.label }}
                </small>
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
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

@media (max-width: 991px) {
  .floating-badge {
    right: 0;
    bottom: -20px;
  }
}
</style>
