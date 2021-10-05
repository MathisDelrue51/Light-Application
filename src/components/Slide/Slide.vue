<template>
  <div class="slide">
    <form>
      <label for="range" class="form-label">Range</label>
      <input
        type="range"
        class="form-range"
        min="1"
        max="240"
        id="range"
        value="200"
      />      
      <input
        type="text"
        class="form-control"
        id="valueRange"
        placeholder="0"
      />
      <button type="submit" class="btn btn-primary">Submit</button>
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
        value="200"
      />
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
    <form>
      <label for="step" class="form-label">Step</label>
      <input
        type="range"
        class="form-range"
        min="1"
        max="240"
        id="step"
        value="200"
      />
      <button type="submit" class="btn btn-primary">Submit</button>
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
export default {
  name: "Slide",
  data() {
    return {
      range: 0,
    };
  },
};
</script>

<style scoped>
</style>