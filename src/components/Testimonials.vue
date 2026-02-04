<script>
export default {
  name: 'Testimonials',
  data() {
    return {
      reviews: [
        { name: 'John Doe', role: 'CEO, TechCorp', text: 'An incredible developer who delivered beyond expectations. The design was stunning and the code was clean.' },
        { name: 'Jane Smith', role: 'Marketing Director', text: 'Professional, timely, and extremely talented. Our website traffic increased by 50% after the redesign.' },
        { name: 'Mike Johnson', role: 'Startup Founder', text: 'Working with this team was a game-changer for our MVP. Highly recommended for any web project.' }
      ]
    }
  }
}
</script>

<template>
  <section id="testimonials" class="py-5">
    <div class="container">
      <h2 class="section-title">Testimonials</h2>
      
      <div id="testimonialCarousel" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div 
            class="carousel-item" 
            v-for="(review, index) in reviews" 
            :key="index"
            :class="{ active: index === 0 }"
          >
            <div class="d-flex justify-content-center">
              <div class="glass-card p-5 text-center col-lg-8">
                <div class="mb-4">
                   <span class="display-1 text-primary opacity-25">"</span>
                </div>
                <p class="lead fst-italic mb-4 text-light">
                  {{ review.text }}
                </p>
                <h5 class="fw-bold mb-1">{{ review.name }}</h5>
                <small class="text-secondary">{{ review.role }}</small>
              </div>
            </div>
          </div>
        </div>
        
        <button class="carousel-control-prev" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.opacity-25 {
  opacity: 0.25;
}
</style>
