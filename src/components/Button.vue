
<template>
  <button class="btn">
    {{ text }}
  </button>
</template>
<script>
export default {
  /* eslint-disable */
  name: "Button",
  props: {
    text: String,
  },
  methods: {
    // onClick() {
    //   console.log("ya");
    // },
  },
};
</script>
<style scoped>
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  /* cursor: pointer; */
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
</style>