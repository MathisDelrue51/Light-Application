<template>
  <div class="slide">

    <colorwheel></colorwheel>

    <form>
      <label for="range" class="form-label">Range</label>
      <input
        type="range"
        class="form-range"
        min="1"
        max="240"
        id="range"
        v-model="valueRange"
      />      
      <input
        type="text"
        class="form-control"
        id="valueRange"
        v-model="valueRange"
      />
      <button type="submit" class="btn btn-primary" v-on:click.prevent="validateRange">Submit</button>
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
      <input
        type="text"
        class="form-control"
        id="valueRange"
        v-model="valueSpeed"
      />
      <button type="submit" class="btn btn-primary" v-on:click.prevent="validateSpeed">Submit</button>
    </form>
    <form>
      <label for="step" class="form-label">Step</label>
      <input
        type="range"
        class="form-range"
        min="1"
        max="240"
        id="step"
        v-model="valueStep"
      />
      <input
        type="text"
        class="form-control"
        id="valueRange"
        v-model="valueStep"
      />
      <button type="submit" class="btn btn-primary" v-on:click.prevent="validateStep">Submit</button>
    </form>

    <div class="btn btn-primary">Mode1</div>
    <div class="btn btn-primary">Mode2</div>
    <div class="btn btn-primary">Mode3</div>
    <div class="btn btn-primary">Mode4</div>
    <div class="btn btn-primary">Mode5</div>
    <div class="btn btn-primary">Mode6</div>
  </div>
</template>

<script>
import Colorwheel from "../Colorwheel/Colorwheel.vue"

export default {
  name: "Slide",
  data() {
    return {
      valueRange:"200",
      valueSpeed:"200",
      valueStep:"200",
    };
  },
  components:{
    'colorwheel': Colorwheel,
  },
  methods:{
    validateRange(){
      console.log("validate range")
      console.log(this.valueRange)
    },
    validateSpeed(){
      console.log("validate speed")
      console.log(this.valueSpeed)
    },
    validateStep(){
      console.log("validate step")
      console.log(this.valueStep)
    },
  }
};
</script>

<style scoped>
</style>