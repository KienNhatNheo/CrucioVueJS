<!-- eslint-disable vue/require-v-for-key -->
<template>
  <ul className="num-summery">
    <li className="num-item" v-for="(item, index) in sumary" :key="index">
      <div className="number">{{ item.num }}</div>
      <div className="role">{{ item.role }}</div>
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      sumary: [
        {
          num: 150,
          role: "Clients",
        },
        {
          num: 620,
          role: "Projects",
        },
        {
          num: 25,
          role: "Awards",
        },
        {
          num: 940,
          role: "Coffee",
        },
      ],
    };
  },
};
</script>
<style>
.num-summery {
  width: 100%;
  height: 20rem;
  background-color: #9933ff;
  text-align: center;
  color: white;
  display: flex;
  padding-left: 15%;
  padding-top: 7%;
}

.num-summery > .num-item {
  width: 20%;
  font-size: 30px;
  font-family: "Open Sans", sans-serif;
  line-height: 4rem;
}

.number {
  letter-spacing: 0.6rem;
}

.role {
  letter-spacing: 0.2rem;
}
</style>
