<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div id="team" class="service" v-if="windowTop > 1500">
    <div class="service-header">OUR TEAM</div>
    <div class="service-hr"></div>
    <ul class="member">
      <li class="out" v-for="(mem, index) in member" :key="index">
        <div :class="'member-prof' + index">
          <div class="ps1">
            <div class="mem-name">{{ mem.name }}</div>
            <div class="mem-role">{{ mem.role }}</div>
            <ul>
              <li v-for="(item, index) in icont" :key="index">
                <iconify-icon :icon="item.name">11</iconify-icon>
              </li>
            </ul>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      windowTop: 0,
      member: [
        {
          name: "SAMANTA L.",
          role: "Architeck",
        },
        {
          name: "PAMELA K.",
          role: "Designer",
        },
        {
          name: "MICHEAL J.",
          role: "Planner",
        },
      ],
      icont: [
        {
          name: "bxl:facebook-square",
        },
        {
          name: "akar-icons:twitter-fill",
        },
        {
          name: "akar-icons:instagram-fill",
        },
        {
          name: "akar-icons:linkedin-box-fill",
        },
      ],
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
li {
  list-style: none;
}
.service {
  text-align: center;
}

.service > .service-header {
  font-size: 32px;
  margin-top: 13rem;
  font-family: "Open Sans", sans-serif;
  letter-spacing: 7px;
}

.service > .service-hr {
  border-bottom: 2px solid purple;
  text-align: center;
  width: 5%;
  margin-left: 47.5%;
  margin-top: 2rem;
}
.member {
  margin-top: 3rem;
  display: flex;
  width: 70%;
  margin-left: 15%;
  overflow: hidden;
  margin-bottom: 10rem;
}

.member-prof0 {
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team1.jpg");
  animation: slide 2s ease-in-out forwards;
}
.member-prof1 {
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team2.jpg");
  animation: slide-3 2s ease-in-out forwards;
}
.member-prof2 {
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/team3.jpg");
  animation: slide-4 2s ease-in-out forwards;
}

.member-prof0:last-child {
  margin-right: 0;
}

.ps1 {
  height: 400px;
  background-color: purple;
  opacity: 0.75;
  visibility: hidden;
  color: white;
}

.member-prof0:hover .ps1 {
  visibility: visible;
}
.member-prof1:hover .ps1 {
  visibility: visible;
}
.member-prof2:hover .ps1 {
  visibility: visible;
}

.member-prof0:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.member-prof1:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.member-prof2:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.out {
  overflow: hidden;
  width: 300px;
  height: 400px;
  margin-right: 7%;
}
.mem-name,
.mem-role {
  position: relative;
  top: 150px;
  margin-bottom: 20px;
}
.ps1 > ul {
  display: flex;
  justify-content: center;
  position: relative;
  top: 180px;
  list-style: none;
}

.ps1 > ul > li {
  margin: 0.7rem;
}
.ps1 > ul > li:hover {
  color: black;
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

@keyframes slide-3 {
  0% {
    opacity: 0;
    transform: translateY(-60%);
  }
  100% {
    opacity: 1;
    transform: translateY(0%);
  }
}

@keyframes slide-4 {
  0% {
    opacity: 0;
    transform: translateX(60%);
  }
  100% {
    opacity: 1;
    transform: translateX(0%);
  }
}
</style>
