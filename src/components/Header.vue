<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div id="header">
    <div class="header-ct1">
      <a href="#"><img class="logo" :src="logo.src1" /></a>
      <button class="btn">Buy now</button>
    </div>
    <div class="header-ct2">
      <a href="#"><img :src="logo.src2" /></a>
      <div class="navbar-collapse">
        <ul class="navbar-nav">
          <li class="nav-item" v-for="(item, index) in content" :key="index">
            <a class="nav-link">{{ item.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      content: [
        { name: "HOME" },
        { name: "ABOUT" },
        { name: "SERVICES" },
        { name: "TEAM" },
        { name: "PORTFOLIO" },
        { name: "BLOG" },
        { name: "CONTACT" },
      ],
      logo: {
        src1: "https://public-assets.envato-static.com/assets/logos/envato_market-a5ace93f8482e885ae008eb481b9451d379599dfed24868e52b6b2d66f5cf633.svg",
        src2: "https://crucio.riccardoborchi.it/wp-content/uploads/2017/05/logo-1.png",
      },
    };
  },
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Helvetica, Arial, "Times New Romand";
}

#header {
  top: 0;
  height: 10rem;
  width: 100%;
  position: fixed;
  z-index: 5;
}
/*Header logo*/
.header-ct1 {
  padding: 0.5rem 1rem;
  height: 3rem;
  display: flex;
  justify-content: space-between;
  background-color: rgb(38, 38, 38);
}

.logo {
  width: 10rem;
  padding: 0.5rem;
}

.btn {
  background-color: rgb(122, 169, 60);
  padding: 0rem 1rem;
  border-radius: 5px;
  color: white;
}
/*Header navbar*/
.header-ct2 {
  background-color: rgb(1, 1, 1);
  height: 7rem;
  display: flex;
  justify-content: space-between;
  padding: 1.5rem 3rem;
  opacity: 0.95;
  border-bottom: 3px solid rgb(45, 5, 64);
}

.header-ct2 > .navbar-collapse > .navbar-nav {
  display: flex;
}

.header-ct2 > .navbar-collapse > .navbar-nav > .nav-item {
  padding: 1rem;
  list-style: none;
}

.header-ct2 > .navbar-collapse > .navbar-nav > .nav-item > .nav-link {
  text-decoration: none;
  color: white;
}
</style>
