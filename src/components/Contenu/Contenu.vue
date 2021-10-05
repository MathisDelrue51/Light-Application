<template>
  <div class="container">
    <div class="btn btn-outline-primary" v-on:click="component = 'balcon'">Balcon</div>
    <div class="btn btn-outline-primary" v-on:click="component = 'salon'">Salon</div>
    <div class="btn btn-outline-primary" v-on:click="component = 'couloir'">Couloir</div>

    <div class="onglet card">

        <component v-bind:is="component"></component>

    </div>
  </div>
</template>

<script>
import Balcon from '../Balcon/Balcon.vue'
import Salon from '../Salon/Salon.vue'
import Couloir from '../Couloir/Couloir.vue'

export default {
  name: "Contenu",
  data: function () {
    return {
        component:"salon",
    };
  },
  components:{
      'balcon':Balcon,
      'salon':Salon,
      'couloir':Couloir,
  },
  methods: {}, 
};
</script>

<style>
.container{    
  margin-top: 100px !important;
}
.onglet {
  height: 80%;
  width:100%,
}
</style>