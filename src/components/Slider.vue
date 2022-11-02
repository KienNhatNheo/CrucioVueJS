<template>
  <div className="introduce">
    <div className="introduce-header">TESTIMONIALS</div>
    <div className="introduce-hr"></div>
    <div class="slides" id="slide-1">
      <div class="introduce-content">
        Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
        tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea
        commodi consequat. Quis aute iure reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur.
      </div>
      <div class="introduce-aut">- Morgan F. -</div>
    </div>
  </div>
</template>
<script></script>
<style scoped>
/* .slider {
    width: 100%;
    height: 300px;
    display: flex;
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
    scroll-snap-type: x mandatory;  
} */
.slides {
  width: 100%;
  flex-shrink: 0;
  height: 100%;
}
/* .slider > div {
    scroll-snap-align: start;
}

.slider > div{
    scroll-behavior: none;
} */

/* .slider::-webkit-scrollbar { 
    width: 0 !important;
    display: none; 
  } */
.slider > div:target {
  transform: scale(0.8);
}

.introduce {
  text-align: center;
  background-color: black;
  color: white;
}
.introduce-content {
  width: 70%;
  margin-left: 15%;
  margin-top: 2rem;
  line-height: 2rem;
  margin-bottom: 1.5rem;
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
</style>
