<template>
  <div class="image-container">
    <img alt="Vue logo" src="./../assets/image.png" />
    <div class="number-layer">
      <NumberChip
        v-for="coord in coords"
        :key="coord.id"
        :x="coord.x"
        :y="coord.y"
        :name="coord.name"
      />
    </div>
  </div>
</template>

<script>
import NumberChip from "./NumberChip.vue";
export default {
  name: "OfficeMap",
  data() {
    return {
      coords: [
        { x: 490, y: 264, id: 1, name: "1" },
        { x: 734, y: 205, id: 2, name: "2" },
        { x: 690, y: 365, id: 3, name: "3" },
      ],
    };
  },
  components: { NumberChip },
};
</script>

<style scoped>
:root {
  --bg-color: rgba(201, 201, 201, 1);
}

.image-container {
  display: flex;
  position: relative;
  flex: 1;
  justify-content: center;
  margin: 16px;
  border-radius: 16px;
  border: 1px solid var(--bg-color);

  -webkit-box-shadow: -2px 6px 26px -10px rgba(201, 201, 201, 1);
  -moz-box-shadow: -2px 6px 26px -10px rgba(201, 201, 201, 1);
  box-shadow: -2px 6px 26px -10px rgba(201, 201, 201, 1);
}
.number-layer {
  position: absolute;
  width: 927px;
  height: 657px;
}
.number {
  position: absolute;
  padding: 4px 8px;
  background-color: white;
  border-radius: 5px;
}
</style>
