<template>
  <div class="testimonial-container">
    <div class="heading-test">
      <p class="pridi">TESTIMONIALS</p>
    </div>
    <div class="testimonial-cards">
      <TestimonialCard
        v-for="testimonial in testimonals"
        :key="testimonial.name"
        :name="testimonial.name"
        :message="testimonial.message"
        :image="testimonial.image"
      />
    </div>
  </div>
</template>

<script>
import TestimonialCard from "./TestimonialCard.vue";

export default {
  name: "testimonial",
  data() {
    return {
      testimonals: [
        {
          name: "Alex P.",
          message:
            "I stumbled upon this shop, and their selection blew me away. The user-friendly website made my shopping experience a breeze!",
          image: "https://i.ibb.co/vmYY6tY/img1.png",
        },
        {
          name: "Emily S.",
          message:
            "The checkout process was seamless, and the responsive design worked flawlessly on my mobile device. I'll definitely be coming back!",
          image: "https://i.ibb.co/k29V4KN/img2.png",
        },
        {
          name: "David R.",
          message:
            "Their site's intuitive navigation made finding the perfect pen a joy. Five stars for both their products and web design!",
          image: "https://i.ibb.co/Mcz1SWT/img3.png",
        },
        {
          name: "Lisa M.",
          message:
            "I appreciate the attention to detail in both their pens and website. A visually stunning and user-focused online shop.",
          image: "https://i.ibb.co/94fW8xZ/img4.png",
        },
      ],
    };
  },
  components: { TestimonialCard },
};
</script>

<style scoped>
.testimonial-container {
  text-align: center;
  padding: 20px;
  min-height: 70vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.heading-test {
  font-size: 40px;
  font-weight: 600;
}

.testimonial-cards {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  padding: 50px 0;
}

@media (max-width: 768px) {
  .testimonial-cards {
    flex-direction: column;
  }
  .heading {
    font-size: 30px;
    font-weight: 500;
  }
}
</style>
