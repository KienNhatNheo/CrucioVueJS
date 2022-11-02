<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div>
    <button @click="isShow">Show</button>
    <div class="bg" v-if="isShowout == true" @click="isShow1">
      <h1>{{ text }}</h1>
      <div class="demo" v-if="isShowout == true">
        <h1>Let's gogogo</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Test",
  props: {
    show: String,
    onclicktext: String,
  },
  data() {
    return {
      text: "hi",
      role: 1,
      parentMessage: "Parent",
      items: [{ message: "Foo" }, { message: "Bar" }],
      isShowout: false,
    };
  },
  methods: {
    Clickfunc() {
      // eslint-disable-next-line vue/no-mutating-props
      this.text = "onclick";
      this.role += 1;
    },
    isShow() {
      this.isShowout = !this.isShowout;
    },
    isShow1() {
      this.$emit("cancel");
    },
  },
};
</script>
<style>
.demo {
  width: 300px;
  height: 300px;
  border: 2px solid black;
}
.bg {
  background: gray;
  opacity: 0.8;
  position: fixed;
  top: 0;
  width: 100%;
  height: 500px;
}
</style>
