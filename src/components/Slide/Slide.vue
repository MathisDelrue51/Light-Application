<template>
  <div class="container">
    <colorwheel></colorwheel>

    <div class="rangeBars">
      <label for="range" class="form-label mt-2">Range</label>
      <div class="valueRangeBar">
        <div class="col-8 me-2">
          <input
            type="range"
            class="form-range me-2"
            min="1"
            max="240"
            id="rangeBar"
            v-model="valueRange"
          />
        </div>
        <div class="col-3">
          <input
            type="text"
            class="form-control"
            id="rangeText"
            v-model="valueRange"
          />
        </div>
      </div>

      <label for="step" class="form-label mt-2">Step</label>
      <div class="valueRangeBar">
        <div class="col-8 me-2">
          <input
            type="range"
            class="form-range me-2"
            min="30"
            max="1000"
            step="5"
            id="speedBar"
            v-model="valueSpeed"
          />
        </div>
        <div class="col-3">
          <input
            type="text"
            class="form-control"
            id="speedText"
            v-model="valueSpeed"
          />
        </div>
      </div>

      <label for="step" class="form-label mt-2">Step</label>
      <div class="valueRangeBar">
        <div class="col-8 me-2">
          <input
            type="range"
            class="form-range me-2"
            min="1"
            max="240"
            id="stepBar"
            v-model="valueStep"
          />
        </div>
        <div class="col-3">
          <input
            type="text"
            class="form-control"
            id="stepText"
            v-model="valueStep"
          />
        </div>
      </div>
    </div>

    <div class="switchMode">
      <div class="btn btn-primary">Mode1</div>
      <div class="btn btn-primary">Mode2</div>
      <div class="btn btn-primary">Mode3</div>
      <div class="btn btn-primary">Mode4</div>
      <div class="btn btn-primary">Mode5</div>
      <div class="btn btn-primary">Mode6</div>
    </div>
  </div>
</template>

<script>
import Colorwheel from "../Colorwheel/Colorwheel.vue";

export default {
  name: "Slide",
  data() {
    return {
      valueRange: "200",
      valueSpeed: "200",
      valueStep: "200",
    };
  },
  components: {
    colorwheel: Colorwheel,
  },
  methods: {
    validateRange() {
      console.log("validate range");
      console.log(this.valueRange);
    },
    validateSpeed() {
      console.log("validate speed");
      console.log(this.valueSpeed);
    },
    validateStep() {
      console.log("validate step");
      console.log(this.valueStep);
    },
  },
};
</script>

<style scoped src='./Slide.css'>
</style>