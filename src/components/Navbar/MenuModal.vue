<template>
  <div>
    <img
      src="../../assets/hamburger.svg"
      alt="hamburger"
      class="hamburger-icon"
      @click="openMenuModal"
    />
    <div
      class="menu-modal"
      v-bind:class="{
        'd-block': isMenuModalOpen,
        'd-none': !isMenuModalOpen,
      }"
      ref="menu"
    >
      <img
        src="../../assets/close.svg"
        alt="close"
        class="close-menu"
        @click="closeMenuModal"
      />
      <div class="links">
        <a href=""> NEW </a>
        <a href="#"> BRANDS </a>
        <a href="#"> COLLECTIONS </a>
        <a href="#"> ACCESSORIES </a>
        <a href="#about-section" @click="closeMenuModal"> ABOUT </a>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "menu-modal",
  props: {
    onClose: Function,
  },
  data() {
    return {
      isMenuModalOpen: false,
    };
  },
  methods: {
    openMenuModal() {
      this.isMenuModalOpen = true;
      gsap.from(this.$refs.menu, { x: 80, duration: 0.5 });
    },
    closeMenuModal() {
      gsap.to(this.$refs.menu, { x: 300, duration: 0.5 }).then(() => {
        this.isMenuModalOpen = false;
        gsap.to(this.$refs.menu, { x: 0, duration: 0.5 });
      });
    },
  },
};
</script>

<style scoped>
.hamburger-icon {
  width: 40px;
  height: 40px;
  padding: 10px;
}
.menu-modal {
  position: fixed;
  top: 90px;
  right: 0;
  width: 50vw;
  max-height: 50%;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  transition: right 0.3s ease-in-out;
  z-index: 1000;
}

.close-menu {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 20px;
  height: 20px;
  cursor: pointer;
}

.links {
  display: flex;
  flex-direction: column;
  padding: 20px;
}

.links a {
  text-decoration: none;
  color: #333;
  font-size: 18px;
  margin-bottom: 10px;
}

.links a:hover {
  color: #007bff;
}

@media (min-width: 768px) {
  .hamburger-icon {
    display: none;
  }
}
</style>
