<template>
  <div>
    <select class="form-select" v-on:change="onChange($event)">
      <option selected>Open this select menu</option>
      <option value="slide">Slide</option>
      <option value="constant">Constant</option>
    </select>

    <div class="btn btn-primary">Eteindre</div>

    <div class="reglages" v-bind:is="component"></div>
  </div>
</template>

<script>
import Slide from "../Slide/Slide.vue";
import Constant from "../Constant/Constant.vue";

export default {
  name: "Salon",
  data() {
    return {
      component: "",
    };
  },
  components: {
    slide: Slide,
    constant: Constant,
  },
  methods: {
    onChange(event) {
      this.component= event.target.value
    },
  },
};
</script>

<style scoped>
.reglages {
  height: 80%;
  width: 100%;
}
</style>