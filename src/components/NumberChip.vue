<template>
  <span class="number" :style="{ top: this.y + 'px', left: this.x + 'px' }">{{
    this.name
  }}</span>
</template>

<script>
export default {
  name: "NumberChip",
  props: {
    name: {
      type: String,
      default: "*",
    },
    x: {
      type: Number,
      required: true,
    },
    y: {
      type: Number,
      required: true,
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.number {
  position: absolute;
  padding: 4px 8px;
  font-weight: bold;
  background-color: white;
  border-radius: 5px;
}
</style>
