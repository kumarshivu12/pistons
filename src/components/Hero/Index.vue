<template>
  <div class="hero">
    <div class="row hero-row-1 m-0 p-0">
      <div class="col-lg-6 col-md-12 order-lg-1">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image1.png" alt="Image" class="image" />
            <div class="overlay-text">
              <div class="content-text">
                <Curved />
                <span class="brand">PISTONS</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-md-12 order-lg-2">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image2.png" alt="Image" class="image" />
            <div class="overlay-text">
              <div class="content-text">
                <span>YOU WERE MADE TO</span>
                <br />
                <span>MAKE AN IMPACT.</span>
                <br />
                <button>SHOP PENS</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row hero-row-2 m-0 p-0">
      <div class="col-lg-6 col-md-12 order-lg-4">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image4.png" alt="Image" class="image" />
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-md-12 order-lg-3">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image3.png" alt="Image" class="image" />
            <div class="overlay-text">
              <div class="content-text">
                <span>MADE FOR THE BEST</span>
                <br />
                <span>CHANGE MAKERS</span>
                <br />
                <button>SHOP BRANDS</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row hero-row-3 m-0 p-0">
      <div class="col-lg-6 col-md-12 order-lg-5">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image5.png" alt="Image" class="image" />
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-md-12 order-lg-5">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image6.png" alt="Image" class="image" />
            <div class="overlay-text">
              <div class="content-text">
                <span>SAVOUR THE PRESENT</span>
                <br />
                <button>SHOP MONT BLANC</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row hero-row-4 m-0 p-0">
      <div class="col-lg-12 col-md-12">
        <div class="content">
          <div class="image-container">
            <img src="../../assets/image7.png" alt="Image" class="image" />
            <div class="overlay-text">
              <div class="content-text">
                <div class="text">WHERE QUALITY MEETS CLASS.</div>
                <br />
                <Curved class="ctext" />
                <span class="brand">PISTONS</span>
                <br />
                <button>SHOP THE FALL 2023 COLLECTION</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

import Curved from "./Curved.vue";
export default {
  name: "Hero",
  components: {
    Curved,
  },

  mounted: function () {
    this.scrollAnimation();
  },
  methods: {
    scrollAnimation() {
      gsap.timeline({
        scrollTrigger: {
          trigger: ".hero-row-1",
          start: "135px 135px",
          end: "bottom 135px",
          markers: false,
          scrub: true,
          pin: true,
          pinSpacing: false,
        },
      });
      gsap.timeline({
        scrollTrigger: {
          trigger: ".hero-row-2",
          start: "135px 135px",
          end: "bottom 135px",
          markers: false,
          scrub: true,
          pin: true,
          pinSpacing: false,
        },
      });
      gsap.timeline({
        scrollTrigger: {
          trigger: ".hero-row-3",
          start: "135px 135px",
          end: "135px 135px",
          markers: false,
          scrub: true,
          pin: true,
          pinSpacing: false,
        },
      });
      // gsap.timeline({
      //   scrollTrigger: {
      //     trigger: ".hero-row-4",
      //     start: "135px 135px",
      //     end: "135px 135px",
      //     markers: false,
      //     scrub: true,
      //     pin: true,
      //     pinSpacing: false,
      //   },
      // });
    },
  },
};
</script>

<style scoped>
svg {
  fill: currentColor;
  transform-origin: center;
  letter-spacing: 2px;
}

.overlay-text {
  font-weight: 400;
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

.content-text {
  text-align: center;
  padding: 10px;
}

.brand {
  color: white;
  font-weight: 700;
  font-family: "Pridi", sans-serif;
  font-size: 2rem;
}
.hero {
  max-width: 100%;
  min-width: 100%;
}
.hero-row-1 {
  z-index: 1;
}
.hero-row-2 {
  z-index: 2;
}
.hero-row-3 {
  z-index: 3;
}
.hero-row-4 {
  z-index: 4;
}
.row > * {
  margin: 0 !important;
  padding: 0 !important;
}

.content {
  max-width: 100%;
}

.image-container {
  position: relative;
}

.image {
  min-width: 100%;
  max-width: 100%;
  max-height: 100%;
  min-height: 100%;
}
.overlay-text {
  font-size: 1.5rem;
  font-weight: 400;
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  color: #fff;
  padding: 10px;
}

.content-text {
  text-align: center;
  color: white;
  padding: 10px;
}

button {
  background-color: white;
  border: 4px solid #ffecc1;
  border-radius: 50px;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 15px;
  margin: 10px;
  cursor: pointer;
  color: #000;
  font-weight: 700;
}

text {
  font-size: 24px;
  font-weight: 400;
  line-height: none;
  letter-spacing: 2px;
}

@media (max-width: 768px) {
  .overlay-text {
    font-size: 10px;
  }

  button {
    font-size: 10px;
    margin: 5px;
    padding: 5px 10px;
  }
}
</style>
