<template>
  <div>
    <vue3-slider v-model="myNumber" />  
  </div>
</template>

<script>
import slider from "vue3-slider"

export default {
  components: {
    "vue3-slider": slider
  }
}
</script>


<style scoped src="./Slider.css"></style>