<template>
  <div class="items-list">
    <SingleItem
      v-for="(item, index) in items"
      :key="item.id"
      :index="index"
      :item="item"
      :model="item.model"
      :maxSpeed="item.maxSpeed"
      :acceleration="item.acceleration"
    />
  </div>
</template>

<script>
import SingleItem from "./item/SingleItem";
export default {
  name: "ItemsList",
  components: { SingleItem },
  props: {
    items: {
      type: Array,
      default: () => [
        {
          id: 1,
          model: "A4 Limousine",
          maxSpeed: 210,
          acceleration: 8.6,
          opinionPool: 73,
        },
        {
          id: 2,
          model: "S4 Limousine",
          maxSpeed: 250,
          acceleration: 4.8,
          opinionPool: 80,
        },
        {
          id: 3,
          model: "S4 Avant",
          maxSpeed: 250,
          acceleration: 4.9,
          opinionPool: 90,
        },
      ],
    },
  },
};
</script>

<style lang="scss" scoped>
.items-list {
  font-family: arial;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-content: space-between;
  max-width: 1200px;
  margin: 20px auto;
}
</style>