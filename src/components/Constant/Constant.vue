<template>
  <div class="container">
    <colorwheel v-on:colorModification="newColor($event)"></colorwheel>
    <div class="btn btn-primary validateButton" @click.prevent="validateColor">Valider</div>
  </div>
</template>

<script>
import Colorwheel from "../Colorwheel/Colorwheel.vue";
import axios from "axios";

export default {
  name: "Constant",
  data() {
    return {
      rValue: 255,
      gValue: 0,
      bValue: 0,
    };
  },
  components: {
    colorwheel: Colorwheel,
  },
  methods: {
    newColor(newColor) {
      this.rValue = newColor.r;
      this.gValue = newColor.g;
      this.bValue = newColor.b;
    },
    validateColor() {
      axios
        .post("http://localhost:3000/constant", {
          mode: "constant",
          rValue: this.rValue,
          gValue: this.gValue,
          bValue: this.bValue,
        })
        .then((reponse) => {
          console.log(reponse.data);
        });
    },
  },
};
</script>

<style scoped>
.validateButton {
  display: block;
  margin: 5% auto;
}
</style>