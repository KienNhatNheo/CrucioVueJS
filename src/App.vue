<template>
  <Header />
  <Banner />
  <welcome />
  <JobAttributed />
  <div class="service">
    <service-intro />
    <service-type />
  </div>
  <started />
  <team-member />
  <sumary />
  <project />
  <subcribe />
  <discuss />
  <Slider />
  <shareholder />
  <contact />
  <footerapp />
  <go-to-top />
</template>

<script>
import Header from "./components/Header.vue";
import Banner from "./components/Banner.vue";
import Welcome from "./components/Welcome.vue";
import JobAttributed from "./components/JobAttributed.vue";
import ServiceIntro from "./components/Service-Intro.vue";
import ServiceType from "./components/Service-Type.vue";
import Started from "./components/Started.vue";
import TeamMember from "./components/TeamMember.vue";
import Sumary from "./components/Sumary.vue";
import Project from "./components/Project.vue";
import Subcribe from "./components/Subcribe.vue";
import Discuss from "./components/Discuss.vue";
import Slider from "./components/Slider.vue";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import Shareholder from "./components/Shareholder.vue";
import Contact from "./components/Contact.vue";
import Footerapp from "./components/Footerapp.vue";
import GoToTop from "./components/GoToTop.vue";
export default {
  name: "App",
  components: {
    Header,
    Banner,
    Welcome,
    JobAttributed,
    ServiceIntro,
    ServiceType,
    Started,
    TeamMember,
    Sumary,
    Project,
    Subcribe,
    Discuss,
    Slider,
    Shareholder,
    Contact,
    Footerapp,
    GoToTop,
  },
};
</script>

<style>
.App {
  text-align: center;
}

.App-logo {
  height: 40vmin;
  pointer-events: none;
}

@media (prefers-reduced-motion: no-preference) {
  .App-logo {
    animation: App-logo-spin infinite 20s linear;
  }
}

.App-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}

.App-link {
  color: #61dafb;
}

@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

service {
  text-align: center;
  margin-bottom: 10rem;
}
</style>
