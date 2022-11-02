<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div id="services" className="service-header">SERVICES</div>
  <div className="service-hr"></div>
  <div className="service-content">
    Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor
    incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
    nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi
    consequat. Quis aute iure reprehenderit in voluptate velit esse cillum
    dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non
    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </div>
</template>
<script></script>
<style>
.service {
  text-align: center;
  margin-bottom: 10rem;
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

.service > .service-content {
  margin-top: 3rem;
  width: 75%;
  margin-left: 12.5%;
  line-height: 30px;
  color: rgb(200, 200, 200);
}
</style>
