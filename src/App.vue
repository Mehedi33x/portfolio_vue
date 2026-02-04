<script>
import Navbar from "./components/Navbar.vue"
import Home from "./components/Home.vue"
import About from "./components/About.vue"
import Services from "./components/Services.vue"
import Skills from "./components/Skills.vue"
import Projects from "./components/Projects.vue"
import Testimonials from "./components/Testimonials.vue"
import Contact from "./components/Contact.vue"
import Footer from "./components/Footer.vue"

export default {
  name: 'App',
  components: {
    Navbar,
    Home,
    About,
    Services,
    Skills,
    Projects,
    Testimonials,
    Contact,
    Footer
  }
}
</script>

<template>
  <div id="app">
    <Navbar />
    <Home />
    <About />
    <Services />
    <Skills />
    <Projects />
    <Testimonials />
    <Contact />
    <Footer />
  </div>
</template>

<style>
/* App-wide critical styles only */
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
