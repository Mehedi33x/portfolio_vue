<script>
export default {
  name: 'Services',
  data() {
    return {
      section: {
        heading: "SERVICES",
        title: "What I Do",
      },

      services: [
        {
          title: "Frontend Dev",
          desc: "Crafting responsive, interactive UIs with Vue.js & React.",
          icon: "fa-laptop-code",
        },
        {
          title: "Backend API",
          desc: "Robust server-side logic using Node.js & Python.",
          icon: "fa-server",
        },
        /* {
          title: "UI/UX Design",
          desc: "User-centered design principles that convert.",
          icon: "fa-wand-magic-sparkles",
        },
        {
          title: "Mobile Apps",
          desc: "Cross-platform mobile solutions used by millions.",
          icon: "fa-mobile-screen",
        }, */
      ],
    }
  },
}
</script>

<template>
  <section id="services" class="py-5">
    <div class="container">
      <h2
        class="section-title text-center"
        :data-heading="section.heading"
      >
        {{ section.title }}
      </h2>

<div class="row g-4 justify-content-center">
        <div
          class="col-md-6 col-lg-3"
          v-for="(service, index) in services"
          :key="index"
        >
          <div class="service-card glass-card p-4 h-100 text-center">
            <div
              class="icon-box mb-4 mx-auto d-flex align-items-center justify-content-center text-white"
            >
              <i
                class="fa-solid fs-3"
                :class="service.icon"
              ></i>
            </div>

            <h4 class="mb-3 fw-bold">
              {{ service.title }}
            </h4>

            <p class="text-secondary mb-0">
              {{ service.desc }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.icon-box {
  width: 70px;
  height: 70px;
  background: linear-gradient(135deg, rgba(255,255,255,0.1), rgba(255,255,255,0.05));
  border-radius: 20px;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.icon-box::after {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 20px;
  padding: 1px;
  background: var(--gradient-main);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
}

.service-card:hover .icon-box {
  background: var(--gradient-main);
  transform: rotate(5deg) scale(1.1);
  box-shadow: 0 0 30px rgba(99, 102, 241, 0.4);
}
</style>
