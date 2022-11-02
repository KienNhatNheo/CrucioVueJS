<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div className="shareholder">
    <div className="img-logo">
      <img
        v-for="(item, index) in img_src"
        :src="item"
        :key="index"
        alt="logo"
      />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      img_src: [
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client1-150x150.png",
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client2-150x150.png",
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client3-132x150.png",
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client4.png",
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client5.png",
        "https://crucio.riccardoborchi.it/wp-content/uploads/2017/03/logo-client6.png",
      ],
    };
  },
};
</script>
<style>
.shareholder {
  height: 12.5rem;
  background-color: rgb(216, 216, 216);
}

.shareholder > .img-logo {
  display: flex;
  justify-content: space-around;
  padding: 4rem 10rem;
}

.shareholder > .img-logo img {
  width: 5rem;
  height: 4rem;
  opacity: 0.6;
}

.shareholder > .img-logo img:hover {
  opacity: 1;
  transition: 1s;
}
</style>
