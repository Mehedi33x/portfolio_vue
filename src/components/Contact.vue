<script>
export default {
  name: 'Contact',
  data() {
    return {
      // Contact form
      form: {
        name: '',
        email: '',
        message: ''
      },

      // Contact info (dynamic)
      contactInfo: [
        { type: 'Email', value: 'mehedihasan33x@gmail.com', icon: 'fa-envelope' },
        { type: 'Location', value: 'Dhaka, Bangladesh', icon: 'fa-location-dot' }
      ],

      // Social links (dynamic)
      socials: [
        { icon: 'fa-github', url: 'https://github.com/mehedi33x' },
        { icon: 'fa-linkedin-in', url: 'https://www.linkedin.com/in/mehedi-hasan-33x/' },
        // { icon: 'fa-twitter', url: 'https://twitter.com/yourusername' },
        // { icon: 'fa-dribbble', url: 'https://dribbble.com/yourusername' }
      ]
    }
  },
  methods: {
    submitForm() {
      alert(`Thanks ${this.form.name}! Message sent.`);
      this.form = { name: '', email: '', message: '' };
    }
  }
}
</script>

<template>
  <section id="contact" class="py-5">
    <div class="container">
      <h2 class="section-title text-center" data-heading="CONTACT">Get In Touch</h2>
      
      <div class="row justify-content-center">
        <!-- Contact Info -->
        <div class="col-lg-5 mb-5 mb-lg-0">
          <div class="h-100 d-flex flex-column justify-content-center">
            <h3 class="fw-bold mb-4">Let's work together!</h3>
            <p class="text-secondary mb-5 fs-5">
              I'm always open to discussing product development work or partnership opportunities.
            </p>
            
            <div class="d-flex flex-column gap-4 mb-5">
              <div
                class="d-flex align-items-center gap-3"
                v-for="(info, index) in contactInfo"
                :key="index"
              >
                <div class="icon-circle">
                  <i class="fa-solid" :class="info.icon + ' text-primary'"></i>
                </div>
                <div>
                  <h6 class="mb-0 fw-bold">{{ info.type }}</h6>
                  <small class="text-secondary">{{ info.value }}</small>
                </div>
              </div>
            </div>

            <div class="d-flex gap-3">
              <a
                v-for="social in socials"
                :key="social.icon"
                :href="social.url"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-outline-light rounded-circle social-btn"
              >
                <i class="fa-brands" :class="social.icon"></i>
              </a>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="col-lg-6">
          <div class="glass-card p-4 p-lg-5">
            <form @submit.prevent="submitForm">
              <div class="form-floating mb-3">
                <input
                  type="text"
                  class="form-control"
                  id="name"
                  placeholder="John Doe"
                  v-model="form.name"
                  required
                >
                <label for="name"><i class="fa-solid fa-user me-2"></i>Name</label>
              </div>
              <div class="form-floating mb-3">
                <input
                  type="email"
                  class="form-control"
                  id="email"
                  placeholder="name@example.com"
                  v-model="form.email"
                  required
                >
                <label for="email"><i class="fa-solid fa-envelope me-2"></i>Email</label>
              </div>
              <div class="form-floating mb-4">
                 <textarea
                   class="form-control"
                   placeholder="Message"
                   id="message"
                   style="height: 150px"
                   v-model="form.message"
                   required
                 ></textarea>
                 <label for="message"><i class="fa-solid fa-comment me-2"></i>Message</label>
              </div>
              <button type="submit" class="btn btn-primary btn-lg w-100 py-3">
                Send Message <i class="fa-solid fa-paper-plane ms-2"></i>
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.icon-circle {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: rgba(255,255,255,0.05);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.25rem;
}
.social-btn {
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}
.social-btn:hover {
  background: var(--gradient-main);
  border-color: transparent;
  transform: translateY(-3px);
}
</style>
