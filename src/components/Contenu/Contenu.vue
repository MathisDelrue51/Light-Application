<template>
  <div class="container">
    <div id="place">
      <div class="btn btn-outline-primary btn-lg" v-on:click="component = 'balcon'">
        Balcon
      </div>
      <div class="btn btn-outline-primary btn-lg" v-on:click="component = 'salon'">
        Salon
      </div>
      <div class="btn btn-outline-primary btn-lg" v-on:click="component = 'couloir'">
        Couloir
      </div>

    </div>

    <div class="card">
      <p>{{ component }}</p>

      <component v-bind:is="component" class="container"></component>
    </div>
  </div>
</template>

<script>
import Balcon from "../Balcon/Balcon.vue";
import Salon from "../Salon/Salon.vue";
import Couloir from "../Couloir/Couloir.vue";

export default {
  name: "Contenu",
  data: function () {
    return {
      component: "salon",
    };
  },
  components: {
    balcon: Balcon,
    salon: Salon,
    couloir: Couloir,
  },
  methods: {},
};
</script>

<style scoped src='./Contenu.css'></style>