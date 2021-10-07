<template>
  <div class="container">
    <div id="selectFunction">
      <select class="form-select form-select-lg me-3" v-on:change="onChange($event)">
      <option selected>Open this select menu</option>
      <option value="slide">Slide</option>
      <option value="constant">Constant</option>
    </select>

    <div class="btn btn-primary btn-lg">Eteindre</div>
    </div>
    

    <div class="container mt-3" v-bind:is="component"></div>
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

<style scoped src='./Salon.css'>

</style>