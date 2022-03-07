
<template>
  <header>
    <div>Items</div>
    <Button text="Add new item" />
  </header>
</template>
<script>
import Button from "./Button";

export default {
  /* eslint-disable */
  name: "Header",
  props: {},
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
