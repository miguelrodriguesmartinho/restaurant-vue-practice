
<template>
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Image</th>
        <th>Sub-category</th>
        <th>Name</th>
        <th>Tags</th>
        <th>Description</th>
        <th>Price</th>
        <th>Available</th>
      </tr>
    </thead>
    <tbody>
      <tr :key="item.id" v-for="item in items">
        <Item
          @delete-item="$emit('delete-item', item.element.id)"
          :item="item"
        />
      </tr>
    </tbody>
  </table>
</template>
<script>
import Item from "./Item";

export default {
  /* eslint-disable */
  name: "Items",
  props: {
    items: Array,
  },
  components: {
    Item,
  },
  emits: ["delete-item"],
};
</script>
<style scoped>
.categories-header {
  display: flex;
  justify-content: space-between;
}
.categories-header div {
  font-weight: bold;
}
.container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
table {
  background: #f4f4f4;
  padding: 10px 20px;
}
</style>