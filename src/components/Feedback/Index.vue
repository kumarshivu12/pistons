<template>
  <div class="feedback">
    <p>FEEDBACK</p>
  </div>
</template>

<script>
export default {
  name: "Feedback",
};
</script>

<style scoped>
p {
  margin: 0;
  padding: 5px;
  letter-spacing: 0.9px;
  color: black;
  font-size: 15px;
  font-weight: bold;
}
.feedback {
  border-top: 2px solid #9a9a9a;
  border-bottom: 2px solid #9a9a9a;
  border-left: 2px solid #9a9a9a;
  position: fixed;
  top: 10rem;
  right: 0;
  margin: 0;
  padding: 0;
  z-index: 8008;
  writing-mode: sideways-lr;
  background: #fff;
  padding-bottom: 5px;
}
</style>
