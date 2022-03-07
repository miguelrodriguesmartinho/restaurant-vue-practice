<template>
  <td>
    <i class="fas fa-times" @click="$emit('delete-item', item.element.id)"></i>
  </td>
  <td>
    <img v-bind:src="item.element.image" alt="food" />
  </td>
  <td>
    {{ item.subCategory }}
  </td>
  <td>
    {{ item.element.title }}
  </td>
  <td>
    <span :key="tag.id" v-for="tag in item.element.items_characteristic_tags"
      >{{ tag.characteristic_tag.label
      }}<span v-if="index != item.element.items_characteristic_tags.length - 1"
        >,
      </span></span
    >
  </td>
  <td>
    {{ item.element.description }}
  </td>
  <td>
    {{ item.element.price + "€" }}
  </td>
</template>
<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "item",
  props: {
    item: Object,
  },
};
</script>
<style scoped>
img {
  width: 50px;
  height: 50px;
  border-radius: 20px;
}

table td {
  padding: 5px;
}

.fas {
  color: red;
}

i {
  cursor: pointer;
}
</style>
