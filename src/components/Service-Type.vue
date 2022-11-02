<!-- eslint-disable vue/require-v-for-key -->
<template>
  <ul className="service-category">
    <li class="service-item" v-for="(item, index) in serviceType1" :key="index">
      <iconify-icon :icon="item.icon"></iconify-icon>
      <div class="service-name">{{ item.name }}</div>
    </li>
  </ul>
  <ul className="service-category">
    <li class="service-item" v-for="(item, index) in serviceType2" :key="index">
      <iconify-icon :icon="item.icon"></iconify-icon>
      <div class="service-name">{{ item.name }}</div>
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      serviceType1: [
        {
          icon: "ion:desktop-outline",
          name: "WEB DESIGN",
        },
        {
          icon: "ion:albums",
          name: "BRAND DESIGN",
        },
        {
          icon: "eva:keypad-fill",
          name: "UI/UX DESIGN",
        },
        {
          icon: "ion:color-palette",
          name: "GRAPHIC DESIGN",
        },
      ],
      serviceType2: [
        {
          icon: "ant-design:camera-filled",
          name: "PHOTOGRAPHY",
        },
        {
          icon: "ic:baseline-videocam",
          name: "VIDEO EDITING",
        },
        {
          icon: "ion:pulse",
          name: "DATA ANALYSIS",
        },
        {
          icon: "bi:person-fill",
          name: "CLIENT ASSISTANCE",
        },
      ],
    };
  },
};
</script>
<style>
.service-category {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 80%;
  margin-left: 10%;
  margin-top: 4rem;
}

.service > .service-category > .service-item {
  list-style: none;
  width: 25%;
}

.service > .service-category > .service-item > iconify-icon {
  color: #9900cc;
  font-size: 40px;
}

.service > .service-category > .service-item > iconify-icon:hover {
  color: #333366;
  cursor: pointer;
  transition: 1.5s ease;
}

.service > .service-category > .service-item > .service-name {
  margin-top: 1rem;
  font-size: 25px;
}
</style>
