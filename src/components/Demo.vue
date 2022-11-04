<template>
  <div className="introduce">
    <div className="introduce-header">TESTIMONIALS</div>
    <div className="introduce-hr"></div>
    <div class="slides" style="text-align: center">
      <carousel
        :items-to-show="1"
        :autoplay="3000"
        :wrapAround="true"
        class="carosel"
      >
        <slide v-for="slide in author_name" :key="slide">
          <div class="introduce-content">
            Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
            tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
            veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex
            ea commodi consequat. Quis aute iure reprehenderit in voluptate
            velit esse cillum dolore eu fugiat nulla pariatur.
            <div class="introduce-aut">{{ slide }}</div>
          </div>
        </slide>

        <template #addons> </template>
      </carousel>
    </div>
  </div>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    // Pagination,
    // Navigation,
  },
  data() {
    return {
      author_name: ["- Morgan F. -", "- Jim P. -", "- John K. -"],
    };
  },
};
</script>
<style scoped>
.slider > div:target {
  transform: scale(0.8);
}

.introduce {
  text-align: center;
  background-color: black;
  color: white;
}
.introduce-content {
  width: 100%;
  margin-top: 2rem;
  line-height: 2rem;
  margin-bottom: 1.5rem;
  text-align: center;
}

.introduce-aut {
  font-style: italic;
  padding-bottom: 7rem;
}
.introduce > .introduce-header {
  padding: 3rem;
  font-size: 32px;
  font-family: "Open Sans", sans-serif;
  letter-spacing: 7px;
}

.introduce > .introduce-hr {
  border-bottom: 5px solid white;
  text-align: center;
  width: 3%;
  margin-left: 48.5%;
}

.carosel {
  margin-left: 15%;
  width: 70%;
  text-align: center;
}
</style>
