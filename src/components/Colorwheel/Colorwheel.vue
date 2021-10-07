<template>
  <div>
    <ColorPicker
      :width="300"
      :height="300"
      :disabled="false"
      startColor="#ff0000"
      @colorChange="onColorChange"
    ></ColorPicker>
    <div class="selected-color-info">
      <p>Selected color:</p>
      <svg height="32" width="32">
        <circle cx="16" cy="16" r="15" :fill="color" />
      </svg>
    </div>
  </div>
</template>

<script>
import ColorPicker from "vue-color-picker-wheel";

export default {
  name: "Colorwheel",
  data() {
    return {
      color: "#ff0000",
    };
  },
  components: {
    ColorPicker,
  },
  methods: {
    onColorChange(newColor) {
      this.color = newColor;
    },
  },
};
</script>

<style scoped src="./Colorwheel.css">
</style>