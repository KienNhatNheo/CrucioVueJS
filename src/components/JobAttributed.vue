<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div class="moreover">
    <div
      :class="'m-item color-' + ++index"
      v-for="(item, index) in attributed"
      :key="index"
    >
      <div class="item-header">{{ item.title }}</div>
      <div class="item-content">{{ item.content }}</div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      attributed: [
        {
          title: "RESPONSIVE",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
        {
          title: "CUSTOMIZABLE",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
        {
          title: "MODERN",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat.",
        },
      ],
    };
  },
};
</script>
<style>
.moreover {
  display: flex;
  color: white;
}

.moreover > .m-item {
  width: 33.33%;
}

.moreover > .m-item > .item-header {
  margin-top: 5rem;
  margin-left: 4.5rem;
  font-size: 30px;
}

.moreover > .m-item > .item-content {
  margin: 1.5rem 5rem 4.5rem 4.5rem;
  text-align: justify;
}

.color-1 {
  background-color: #9900ff;
}

.color-2 {
  background-color: #cc00ff;
}

.color-3 {
  background-color: #990099;
}
</style>
