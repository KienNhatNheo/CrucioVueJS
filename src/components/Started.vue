<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div class="started" v-if="windowTop > 800">
    <div class="started-content">WE CREATE AWESOME PROJECTS</div>
    <div class="started-button">GET STARTED</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      windowTop: 0,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
    },
  },
};
</script>
<style>
.started {
  width: 100%;
  height: 23.5rem;
  background-color: #9933ff;
  text-align: center;
  color: white;
}

.started > .started-content {
  position: absolute;
  margin-top: 8rem;
  margin-left: 20%;
  width: 60%;
  font-size: 40px;
  font-family: "Open Sans", sans-serif;
  letter-spacing: 7px;
  animation: slide 2s ease-in-out forwards;
}

.started > .started-button {
  position: absolute;
  position: absolute;
  margin-top: 14rem;
  margin-left: 43.5%;
  width: 13%;
  padding: 0.8rem;
  font-size: 16px;
  border: 3px solid white;
  letter-spacing: 2px;
  animation: slide-button 2s ease-in-out forwards;
}

.started > .started-button:hover {
  background-color: white;
  color: #9933ff;
  transition: 1s ease;
}

@keyframes slide {
  0% {
    opacity: 0;
    transform: translateX(-60%);
  }
  100% {
    opacity: 1;
    transform: translateX(0%);
  }
}

@keyframes slide-button {
  0% {
    opacity: 0;
    transform: translateY(50%);
  }
  100% {
    opacity: 1;
    transform: translateY(0%);
  }
}
</style>
