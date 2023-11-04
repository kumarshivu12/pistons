<template>
  <div>
    <img
      src="../../assets/search.svg"
      alt="search"
      @click="openSearchModal"
      class="search-logo"
    />
    <div
      class="search-modal"
      v-bind:class="{
        'd-block': isSearchModalOpen,
        'd-none': !isSearchModalOpen,
      }"
      ref="search"
    >
      <img
        src="../../assets/close.svg"
        alt="close"
        class="close-search"
        @click="closeSearchModal"
      />
      <div class="search">
        <input placeholder="Search..." />
        <button class="button">Search</button>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "search-model",
  props: {
    onClose: Function,
  },
  data() {
    return {
      isSearchModalOpen: false,
    };
  },
  methods: {
    openSearchModal() {
      this.isSearchModalOpen = true;
      if (window.innerWidth >= 700) {
        gsap.from(this.$refs.search, { x: 150, duration: 0.5 });
      } else {
        gsap.from(this.$refs.search, { y: -100, duration: 0.5 });
      }
    },
    closeSearchModal() {
      if (window.innerWidth >= 700) {
        gsap.to(this.$refs.search, { x: 500, duration: 0.5 }).then(() => {
          this.isSearchModalOpen = false;
          gsap.to(this.$refs.search, { x: 10, duration: 0.5 });
        });
      } else {
        gsap.to(this.$refs.search, { y: -130, duration: 0.5 }).then(() => {
          this.isSearchModalOpen = false;
          gsap.to(this.$refs.search, { y: 0, duration: 0.5 });
        });
      }
    },
  },
};
</script>

<style scoped>
.search-logo {
  width: 40px;
  height: 40px;
  padding: 10px;
}
.search-modal {
  position: absolute;
  top: 90px;
  right: 70px;
  z-index: 1050;
  width: 400px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15);
  padding: 5px 20px;
}

.close-search {
  cursor: pointer;
  width: 20px;
  height: 20px;
  margin: 5px;
  margin-left: 95%;
}

.search input {
  width: 200px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 20px;
}

.button {
  padding: 10px 40px;
  background-color: black;
  color: #fff;
  border: none;
  border-radius: 20px;
  cursor: pointer;
  width: 150px;
  text-align: center;
}

.search {
  display: flex;
  justify-content: space-between;
  margin: 5px 0;
  text-align: center;
}
</style>
