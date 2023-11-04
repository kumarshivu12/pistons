<template>
  <div class="testimonial-card">
    <div class="testimonial-image" :style="`background-image: url(${image});`">
      <p class="testimonial-name">{{ name }}</p>
    </div>
    <div class="testimonial-content">
      <p class="testimonial-message">{{ message }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "testimonal-card",
  props: {
    name: String,
    message: String,
    image: String,
  },
};
</script>

<style scoped>
.testimonial-card {
  background-color: black;
  border-radius: 10px;
  width: 250px;
  height: 250px;
  overflow: hidden;
  position: relative;
  cursor: pointer;
}

.testimonial-image {
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.testimonial-content {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 10px;
  background-color: black;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.testimonial-card:hover .testimonial-content {
  opacity: 1;
}

.testimonial-message {
  text-align: center;
}

.testimonial-name {
  color: white;
  font-size: 20px;
  font-weight: 600;
}
</style>
