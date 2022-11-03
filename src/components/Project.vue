eslint-disable vue/require-v-for-key
<template>
  <div v-if="windowTop > 3400">
    <div id="portfolio" class="service">
      <div class="service-header">OUR PORTFOLIO</div>
      <div class="service-hr"></div>
      <div class="task-bar">
        <div class="task-item" v-for="(item, index) in classify" :key="index">
          <div @click="changetask(item.img_id)">{{ item.name }}</div>
        </div>
      </div>
      <div class="material">
        <div class="m-out" v-for="(item, index) in current_img" :key="index">
          <div :class="'mtr-' + item">
            <div class="ps">
              <div class="m-name big">{{ project[item - 1].name }}</div>
              <div class="m-role">{{ project[item - 1].des }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mbutton-bg" v-if="loadmorebutton == true">
      <div class="material-button" @click="showAll">LOAD MORE</div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      current_img: [1, 2, 3, 4, 5, 6, 7, 8],
      loadmorebutton: true,
      project: [
        {
          name: "Project #1",
          des: "Project Description",
        },
        {
          name: "Project #2",
          des: "Project Description",
        },
        {
          name: "Project #3",
          des: "Project Description",
        },
        {
          name: "Project #4",
          des: "Project Description",
        },
        {
          name: "Project #5",
          des: "Project Description",
        },
        {
          name: "Project #6",
          des: "Project Description",
        },
        {
          name: "Project #7",
          des: "Project Description",
        },
        {
          name: "Project #8",
          des: "Project Description",
        },
        {
          name: "Project #9",
          des: "Project Description",
        },
      ],
      windowTop: 0,
      classify: [
        {
          name: "All",
          img_id: [1, 2, 3, 4, 5, 6, 7, 8],
        },
        {
          name: "Graphic Design",
          img_id: [1, 2, 3],
        },
        {
          name: "Web Design",
          img_id: [4, 5, 6],
        },
        {
          name: "Web Development",
          img_id: [7, 8],
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
    // eslint-disable-next-line no-unused-vars
    changetask(img_id) {
      this.current_img = img_id;
      this.loadmorebutton = true;
    },
    showAll() {
      this.current_img = [1, 2, 3, 4, 5, 6, 7, 8, 9];
      this.loadmorebutton = false;
    },
  },
};
</script>
<style scoped>
.service {
  text-align: center;
  margin-bottom: 0rem;
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

.task-bar {
  display: flex;
  margin-top: 2rem;
  justify-content: center;
}

.task-bar > .task-item {
  margin: 1.7rem;
  cursor: pointer;
}

.material {
  display: flex;
  flex-wrap: wrap;
}

.mtr-1 {
  width: 100%;
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work1.jpg");
  background-size: cover;
  animation: slide 1s ease-in-out forwards;
}
.mtr-2 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work2.jpg");
  animation: slide-r 1s ease-in-out forwards;
}
.mtr-3 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work3.jpg");
  animation: slide-u 1s ease-in-out forwards;
}
.mtr-4 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work4.jpg");
  animation: slide 1s ease-in-out forwards;
}
.mtr-5 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work5.jpg");
  animation: slide-r 1s ease-in-out forwards;
}
.mtr-6 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work6.jpg");
  animation: slide-u 1s ease-in-out forwards;
}
.mtr-7 {
  width: 100%;
  overflow: hidden;
  background-size: cover;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work7.jpg");
  animation: slide 1s ease-in-out forwards;
}
.mtr-8 {
  width: 100%;
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work8.jpg");
  background-size: cover;
  animation: slide-r 1s ease-in-out forwards;
}
.mtr-9 {
  width: 100%;
  overflow: hidden;
  background-image: url("https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/work8.jpg");
  background-size: cover;
  animation: slide-r 1s ease-in-out forwards;
}
.mtr-1:hover .ps {
  visibility: visible;
}

.mtr-1:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.mtr-2:hover .ps {
  visibility: visible;
}

.mtr-2:hover {
  transform: scale(1.2);
  transition: 2s ease;
}

.mtr-3:hover .ps {
  visibility: visible;
}

.mtr-3:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.mtr-4:hover .ps {
  visibility: visible;
}

.mtr-4:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.mtr-5:hover .ps {
  visibility: visible;
}

.mtr-5:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.mtr-6:hover .ps {
  visibility: visible;
}

.mtr-6:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.mtr-7:hover .ps {
  visibility: visible;
}

.mtr-7:hover {
  transform: scale(1.2);
  transition: 2s ease;
}

.mtr-8:hover .ps {
  visibility: visible;
}

.mtr-8:hover {
  transform: scale(1.2);
  transition: 2s ease;
}

.mtr-9:hover .ps {
  visibility: visible;
}

.mtr-9:hover {
  transform: scale(1.2);
  transition: 2s ease;
}
.m-out {
  overflow: hidden;
  width: 25%;
}

.ps {
  height: 260px;
  background-color: purple;
  opacity: 0.75;
  visibility: hidden;
  color: white;
}

.m-name,
.m-role {
  position: relative;
  top: 100px;
  margin-bottom: 20px;
}
.big {
  font-size: 30px;
}
.material-button {
  text-align: center;
  margin-left: 44%;
  width: 12%;
  border: 3px solid black;
  padding: 0.6rem;
  letter-spacing: 0.1rem;
}
.material-button:hover {
  background-color: black;
  color: white;
  transition: 1s ease;
}
div.service:last-child {
  margin-bottom: 0;
}

.task-item:hover {
  color: purple;
}

.active {
  color: purple;
}

.mbutton-bg {
  padding: 3rem;
  background-color: rgb(216, 216, 216);
  margin-bottom: 10rem;
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
@keyframes slide-u {
  0% {
    opacity: 0;
    transform: translateY(50%);
  }
  100% {
    opacity: 1;
    transform: translateY(0%);
  }
}
@keyframes slide-d {
  0% {
    opacity: 0;
    transform: translateY(-50%);
  }
  100% {
    opacity: 1;
    transform: translateY(0%);
  }
}
@keyframes slide-r {
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
