<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div>
    <div class="footer">
      <div>
        <a href="#"
          ><img
            src="https://crucio.riccardoborchi.it/wp-content/uploads/2017/05/logo-1.png"
            alt="logo"
        /></a>
      </div>
      <div class="logo-task">
        <ul>
          <li v-for="(item, index) in icon" :key="index">
            <a href="#"><iconify-icon :icon="item"></iconify-icon></a>
          </li>
        </ul>
      </div>
    </div>
    <div class="footer-end">© 2017. Crucio. All Rights Reserved.</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      icon: [
        "bxl:facebook-square",
        "akar-icons:twitter-fill",
        "akar-icons:instagram-fill",
        "akar-icons:linkedin-box-fill",
        "akar-icons:dribbble-fill",
        "akar-icons:youtube-fill",
      ],
    };
  },
};
</script>
<style>
.footer {
  background-color: rgb(1, 1, 1);
  height: 15rem;
  margin-top: 20rem;
  padding: 0 10rem;
  padding-top: 3rem;
  text-align: center;
}

.footer div {
  padding-bottom: 2rem;
}

.footer > .logo-task {
  text-align: center;
}

.footer > .logo-task ul {
  display: flex;
  color: white;
  list-style: none;
  justify-content: center;
}

.footer > .logo-task li {
  padding-left: 3rem;
}

.footer > .logo-task ul li a {
  color: white;
}

.footer > .logo-task ul li a iconify-icon {
  font-size: 1.8rem;
}

.footer > .logo-task ul li a:hover {
  color: purple;
  transition: 1s ease;
}
.footer-end {
  text-align: center;
  background-color: purple;
  color: white;
  padding: 0.7rem;
  letter-spacing: 0.1rem;
  font-size: 13px;
}
</style>
