<template>
  <div>
    <div class="head">FREE SHIPPING ON ALL ORDERS</div>

    <div class="navbar-container">
      <p class="pridi">PISTONS</p>
      <div class="navbar-links">
        <a href=""> NEW </a>
        <a href="#"> BRANDS </a>
        <a href="#"> COLLECTIONS </a>
        <a href="#"> ACCESSORIES </a>
        <a href="#about-section"> ABOUT </a>
      </div>
      <div class="navbar-icons">
        <img src="../../assets/cart.svg" alt="cart" />

        <SearchModal />

        <MenuModal />
      </div>
    </div>
  </div>
</template>

<script>
import MenuModal from "./MenuModal.vue";
import SearchModal from "./SearchModal.vue";

export default {
  name: "Navbar",
  components: { SearchModal, MenuModal },
};
</script>

<style scoped>
.head {
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  width: 100%;
  background-color: #e3e3e3;
  font-size: 16px;
  font-weight: 700;
  padding: 15;
  color: #9a9a9a;
  height: 40px;
  position: fixed;
  z-index: 5000;
  top: 0;
}
.navbar-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 20px;
  height: 70px;
  position: fixed;
  min-width: 100vw;
  top: 40px;
  background-color: #fff;
  z-index: 1000;
}
.navbar-container p {
  font-size: 30px;
  font-weight: 600;
}
.navbar-container p {
  font-family: "Pridi";
  margin-top: 10px;
}
.navbar-links a {
  padding: 10px;
  text-decoration: none;
  color: black;
  font-weight: 500;
  cursor: pointer;
}

.navbar-icons {
  display: flex;
  cursor: pointer;
}
.navbar-icons img {
  width: 40px;
  height: 40px;
  padding: 10px;
}
.links a:hover {
  color: #007bff;
}
@media (max-width: 768px) {
  .navbar-links {
    display: none;
  }
}
</style>
