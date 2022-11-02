<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div id="about" class="welcome">
    <div className="welcome-header">WELCOME TO <span>CRUCIO</span></div>
    <div className="welcome-intro">WE CREATE AWESOME WEBSITES</div>
    <div className="welcome-content">
      Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor
      incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
      nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi
      consequat. Quis aute iure reprehenderit in voluptate velit esse cillum
      dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non
      proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </div>
  </div>
</template>

<script></script>
<style>
.welcome {
  text-align: center;
  width: 70%;
  margin-left: 15%;
}
.welcome > .welcome-header {
  margin-top: 13rem;
  font-size: 45px;
  letter-spacing: 5px;
  margin-bottom: 2.5rem;
  font-family: "Open Sans", sans-serif;
}
.welcome > .welcome-intro {
  font-size: 30px;
  letter-spacing: 10px;
  font-weight: bold;
  margin-bottom: 3rem;
}
.welcome > .welcome-content {
  line-height: 30px;
  color: rgb(216, 216, 216);
  margin-bottom: 13rem;
}
</style>
