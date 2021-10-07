<template>
  <div class="container">
    <colorwheel></colorwheel>

    <div class="rangeBars">
      <form>
        <label for="range" class="form-label mt-2">Range</label>
        <input
          type="range"
          class="form-range"
          min="1"
          max="240"
          id="range"
          v-model="valueRange"
        />
        <div class="valueRangeBar mt-2">
          <input
            type="text"
            class="form-control me-2"
            id="valueRange"
            v-model="valueRange"
          />
          <button
            type="submit"
            class="btn btn-primary"
            v-on:click.prevent="validateRange"
          >
            Submit
          </button>
        </div>
      </form>

      <form>
        <label for="speed" class="form-label">Speed</label>

        <input
          type="range"
          class="form-range"
          min="30"
          max="1000"
          step="5"
          id="speed"
          v-model="valueSpeed"
        />
        <div class="valueRangeBar mt-2">
          <input
            type="text"
            class="form-control me-2"
            id="valueRange"
            v-model="valueSpeed"
          />
          <button
            type="submit"
            class="btn btn-primary"
            v-on:click.prevent="validateSpeed"
          >
            Submit
          </button>
        </div>
      </form>
      <form>
        <label for="step" class="form-label mt-2">Step</label>
        <input
          type="range"
          class="form-range"
          min="1"
          max="240"
          id="step"
          v-model="valueStep"
        />
        <div class="valueRangeBar mt-2">
          <input
            type="text"
            class="form-control me-2"
            id="valueRange"
            v-model="valueStep"
          />
          <button
            type="submit"
            class="btn btn-primary"
            v-on:click.prevent="validateStep"
          >
            Submit
          </button>
        </div>
      </form>
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