<template>
  <div class="categories-container">
    <img src="..\images\minus.png" alt="minus circle" />
    <img class="margin-right-25" src="..\images\plus.png" alt="plus circle" />

    <div
      class="d-flex"
      @click="$emit('update-category', categorie.title)"
      :key="categorie.id"
      v-for="categorie in categories"
      v-bind:class="{ selected: categorie.title == this.selectedC }"
    >
      <span>{{ categorie.title }}</span>
      <img v-bind:src="categorie.image" alt="plus circle" />
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Categories",
  props: {
    categories: Array,
    selectedC: String,
  },
};
</script>

<style scoped>
.categories-container {
  display: flex;
  flex-direction: row;
  margin-bottom: 25px;
  margin-left: 20px;
}

.categories-container img {
  height: 35px;
  width: 35px;
  border-radius: 50%;
  margin-right: 10px;
}

.btn {
  display: block;
}

.margin-right-25 {
  margin-right: 25px !important;
}

.d-flex {
  flex-direction: column;
  margin-right: 10px;
}

.d-flex img {
  align-self: center;
  cursor: pointer;
}

.selected {
  background-color: rgba(255, 174, 0, 0.753);
  color: whitesmoke;
  font-weight: bold;
  padding: 5px;
  border-radius: 10px;
}
</style>