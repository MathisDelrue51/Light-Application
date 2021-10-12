<template>
  <div class="container">
    <colorwheel v-on:colorModification="newColor($event)"></colorwheel>

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
      <div class="btn btn-primary" @click.prevent="switchToMode1">Mode1</div>
      <div class="btn btn-primary" @click.prevent="switchToMode2">Mode2</div>
      <div class="btn btn-primary" @click.prevent="switchToMode3">Mode3</div>
      <div class="btn btn-primary" @click.prevent="switchToMode4">Mode4</div>
      <div class="btn btn-primary" @click.prevent="switchToMode5">Mode5</div>
      <div class="btn btn-primary" @click.prevent="switchToMode6">Mode6</div>
    </div>
  </div>
</template>

<script>
import Colorwheel from "../Colorwheel/Colorwheel.vue";
import axios from "axios";

export default {
  name: "Slide",
  data() {
    return {
      mode: "mode 1",
      valueRange: 200,
      valueSpeed: 200,
      valueStep: 200,
      rValue: 255,
      gValue: 0,
      bValue: 0,
    };
  },
  components: {
    colorwheel: Colorwheel,
  },
  methods: {
    switchToMode1() {
      this.mode = "mode 1";
      axios
        .post("http://localhost:3000/mode1", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    switchToMode2() {
      this.mode = "mode 2";
      axios
        .post("http://localhost:3000/mode2", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    switchToMode3() {
      this.mode = "mode 3";
      axios
        .post("http://localhost:3000/mode3", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    switchToMode4() {
      this.mode = "mode 4";
      axios
        .post("http://localhost:3000/mode4", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    switchToMode5() {
      this.mode = "mode 5";
      axios
        .post("http://localhost:3000/mode5", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    switchToMode6() {
      this.mode = "mode 6";
      axios
        .post("http://localhost:3000/mode6", {
          mode: this.mode,
          valueRange: this.valueRange,
          valueSpeed: this.valueSpeed,
          valueStep: this.valueStep,
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
    newColor(newColor) {
      this.rValue = newColor.r;
      this.gValue = newColor.g;
      this.bValue = newColor.b;
    },
  },
};
</script>

<style scoped src='./Slide.css'>
</style>