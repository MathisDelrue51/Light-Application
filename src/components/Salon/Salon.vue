<template>
  <div>
    <select class="form-select" aria-label="Default select example">
      <option selected>Open this select menu</option>
      <option value="Slide" v-on:click="component = 'slide'">Slide</option>
      <option value="Constant" v-on:click="component = 'constant'">Constant</option>
    </select>

    <div class="btn btn-primary">Eteindre</div>

    <div class="reglages" v-bind:is="component"></div>
  </div>
</template>

<script>
import Slide from '../Slide/Slide.vue'
import Constant from '../Constant/Constant.vue'

export default {
  name: "Salon",
  data() {
    return {
      component: "",
    };
  },
  components: {
    'slide': Slide,
    'constant': Constant,
  },
};
</script>

<style scoped>
.reglages{
    height: 80%;
    width: 100%;
}
</style>