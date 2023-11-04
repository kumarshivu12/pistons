<template>
  <div class="about-container" id="about-section">
    <div class="image-container">
      <img src="../../assets/about1.png" alt="about1" class="about-image" />
    </div>
    <div class="text-container">
      <p class="about-title pridi">ABOUT PISTONS</p>
      <p>
        Established in 1897, our beloved fountain pen haven, 'PISTONS,' has been
        a haven for pen enthusiasts for generations. With a century-long
        dedication to fine writing instruments, we've bridged tradition and
        modernity, offering a curated selection of vintage and contemporary
        fountain pens. Our little shop, nestled in the heart of town, continues
        to inspire a love for the art of writing, connecting past and present
        through the timeless elegance of ink on paper.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "about",
};
</script>

<style scoped>
.about-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: center;
  text-align: center;
  min-height: 75vh;
  padding: 20px;
}
.image-container {
  text-align: center;
  padding: 20px;
}

.about-image {
  max-width: 100%;
  height: auto;
}

.text-container {
  text-align: left;
  padding: 20px;
}

.about-title {
  font-size: 25px;
  font-weight: 500;
  text-align: center;
}

@media (max-width: 768px) {
  .about-container {
    grid-template-columns: 1fr;
  }

  .text-container {
    text-align: center;
    padding: 20px;
  }
}
</style>
