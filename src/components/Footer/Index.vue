<template>
  <div class="footer-container">
    <p class="header pridi">PISTONS</p>
    <p class="heading">STAY CONNECTED</p>
    <div class="social-icons">
      <img src="../../assets/facebook.svg" alt="facebook" />
      <img src="../../assets/youtube.svg" alt="youtube" />
      <img src="../../assets/instagram.svg" alt="instagram" />
      <img src="../../assets/twitter.svg" alt="twitter" />
      <img src="../../assets/gmail.svg" alt="gmail" />
    </div>
  </div>
</template>

<script>
export default {
  name: "foot-er",
};
</script>

<style scoped>
.footer-container {
  background: black;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 50px;
  text-align: center;
}
.heading {
  margin: 20px 0;
  font-size: 20px !important;
  font-weight: 600;
}
.header {
  margin-bottom: 20px;
  font-size: 50px;
  font-weight: 600;
}
.social-icons {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
.social-icons img {
  margin: 10px;
  font-weight: 600;
}
</style>
