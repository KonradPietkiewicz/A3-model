<template>
  <div class="single-item">
    <p>Audi {{ index + 1 }}</p>
    <p>Model: {{ model }}</p>
    <p>Prędkość maksymalna: {{ maxSpeedWithKm }}</p>
    <p>Przyspieszenie 0-100 km/h: {{ accelerationWithS }}</p>
    <div v-if="item.opinionPool">
      Opinia modelu:
      <progress max="100" :value="item.opinionPool"></progress>
      {{ item.opinionPool }}%
    </div>
  </div>
</template>

<script>
import { computed } from "vue";
export default {
  name: "SingleItem",
  props: {
    item: {
      type: Object,
      default: () => ({}),
    },
    index: {
      type: Number,
      default: 0,
    },
    model: {
      type: String,
      default: "",
    },
    maxSpeed: {
      type: Number,
      default: 0,
    },
    acceleration: {
      type: Number,
      default: 0,
    },
  },
  setup(props) {
    const maxSpeedWithKm = computed(() => `${props.maxSpeed} km/h`);
    const accelerationWithS = computed(() => `${props.acceleration} s`);

    return { maxSpeedWithKm, accelerationWithS };
  },
};
</script>

<style lang="scss" scoped>
.single-item {
  border: 1px solid black;
  padding: 10px;
  margin: 20px;
}
</style>