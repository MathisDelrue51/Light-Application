<template>
  <div class="container">
    <ColorPicker
      :width="width"
      :height="height"
      :disabled="false"
      @colorChange="onColorChange"
      v-model="color"
    ></ColorPicker>
    <div class="selected-color-info">
      <p>Selected color: {{ color }}</p>
      <svg height="32" width="32">
        <circle cx="16" cy="16" r="15" :fill="color" />
      </svg>
    </div>

    <div class="selected-color-rbg">
      <input
        type="text"
        class="form-control me-2"
        id="rgb-r"
        v-model="rValue"
      />
      <input
        type="text"
        class="form-control me-2"
        id="rgb-g"
        v-model="gValue"
      />
      <input
        type="text"
        class="form-control me-2"
        id="rgb-b"
        v-model="bValue"
      />
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
      height: 250,
      width: 250,
      rValue: 255,
      gValue: 0,
      bValue: 0,
    };
  },
  components: {
    ColorPicker,
  },
  methods: {
    onColorChange(newColor) {
      this.color = newColor;
      this.hexToRGB(newColor);
    },
    hexToRGB(hex) {
      // Expand shorthand form (e.g. "03F") to full form (e.g. "0033FF")
      var shorthandRegex = /^#?([a-f\d])([a-f\d])([a-f\d])$/i;
      hex = hex.replace(shorthandRegex, function (m, r, g, b) {
        return r + r + g + g + b + b;
      });

      var result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);

      this.rValue = parseInt(result[1], 16);
      this.gValue = parseInt(result[2], 16);
      this.bValue = parseInt(result[3], 16);
    },
    rgbToHex() {
      this.color =
        "#" +
        ((1 << 24) + (+this.rValue << 16) + (+this.gValue << 8) + +this.bValue)
          .toString(16)
          .slice(1);
    },
  },
  watch: {
    rValue: function () {
      this.rgbToHex();
    },
    gValue: function () {
      this.rgbToHex();
    },
    bValue: function () {
      this.rgbToHex();
    },
  },
};
</script>

<style scoped src="./Colorwheel.css">
</style>