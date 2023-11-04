<template>
  <div>
    <Feedback />
    <Navbar />
    <Hero />
    <About />
    <Testimonal />
    <Footer />
  </div>
</template>

<script>
import Navbar from "./components/Navbar/Index.vue";
import Hero from "./components/Hero/Index.vue";
import Footer from "./components/Footer/Index.vue";
import About from "./components/About/Index.vue";
import Testimonal from "./components/Testimonials/Index.vue";
import Feedback from "./components/Feedback/Index.vue";
export default {
  name: "App",
  components: {
    Navbar,
    Hero,
    About,
    Footer,
    Testimonal,
    Feedback,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Oxygen:wght@300;400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Pridi:wght@200;300;400;500;600;700&display=swap");
</style>
