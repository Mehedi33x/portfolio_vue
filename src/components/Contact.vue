<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Logic for form submission
      alert(`Message from ${this.form.name} sent! (Demo)`);
      this.form = { name: '', email: '', message: '' };
    }
  }
}
</script>

<template>
  <section id="contact" class="py-5 bg-darker">
    <div class="container">
      <h2 class="section-title">Get In Touch</h2>
      
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="glass-card p-4 p-lg-5">
            <form @submit.prevent="submitForm">
              <div class="row g-3">
                <div class="col-md-6">
                  <div class="form-floating text-dark">
                    <input type="text" class="form-control" id="name" placeholder="Your Name" v-model="form.name" required>
                    <label for="name">Your Name</label>
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="form-floating text-dark">
                    <input type="email" class="form-control" id="email" placeholder="Your Email" v-model="form.email" required>
                    <label for="email">Your Email</label>
                  </div>
                </div>
                <div class="col-12">
                  <div class="form-floating text-dark">
                    <textarea class="form-control" placeholder="Leave a comment here" id="message" style="height: 150px" v-model="form.message" required></textarea>
                    <label for="message">Message</label>
                  </div>
                </div>
                <div class="col-12 text-center mt-4">
                  <button type="submit" class="btn btn-primary btn-lg w-100">Send Message</button>
                </div>
              </div>
            </form>
            
            <div class="text-center mt-5">
              <p class="text-secondary mb-3">Or connect with me on</p>
              <div class="d-flex justify-content-center gap-3">
                 <a href="#" class="btn btn-outline-light rounded-circle p-2" style="width: 45px; height: 45px;"><i class="bi bi-github"></i> G</a>
                 <a href="#" class="btn btn-outline-light rounded-circle p-2" style="width: 45px; height: 45px;"><i class="bi bi-linkedin"></i> L</a>
                 <a href="#" class="btn btn-outline-light rounded-circle p-2" style="width: 45px; height: 45px;"><i class="bi bi-twitter"></i> T</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.form-control {
  border: none;
  background: rgba(255, 255, 255, 0.9);
}

.form-control:focus {
  box-shadow: 0 0 0 4px rgba(108, 99, 255, 0.2);
}
</style>
