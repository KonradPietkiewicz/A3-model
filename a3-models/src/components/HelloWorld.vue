<template>
  <ItemsList :items="models" />
</template>
<script>
import { ref } from "vue";
import ItemsList from "./items/ItemsList";
export default {
  name: "HelloWorld",
  components: {
    ItemsList,
  },
  setup() {
    const models = ref([
      {
        id: 1,
        model: "A3 Sportback",
        maxSpeed: 220,
        acceleration: 8.2,
        opinionPool: 70,
      },
      {
        id: 2,
        model: "A3 Limousine",
        maxSpeed: 224,
        acceleration: 8.2,
        opinionPool: 75,
      },
      {
        id: 3,
        model: "S3 Limousine ",
        maxSpeed: 250,
        acceleration: 4.7,
        opinionPool: 80,
      },
      {
        id: 4,
        model: "S3 Sportback",
        maxSpeed: 220,
        acceleration: 4.7,
        opinionPool: 85,
      },
      {
        id: 5,
        model: "RS3 Sportback",
        maxSpeed: 220,
        acceleration: 4.1,
        opinionPool: 90,
      },
      {
        id: 6,
        model: "RS3 Limousine",
        maxSpeed: 220,
        acceleration: 8.2,
        opinionPool: 95,
      },
    ]);

    return { models };
  },
};
</script>

<style lang="scss">
</style>

