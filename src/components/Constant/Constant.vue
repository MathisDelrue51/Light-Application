<template>
    <div class="constant">
        <colorwheel></colorwheel>
        <div class="btn btn-primary">Valider</div>
    </div>
</template>

<script>
import Colorwheel from "../Colorwheel/Colorwheel.vue"

export default {
    name:"Constant",    
    components:{
    'colorwheel': Colorwheel,
  },
}
</script>

<style scoped>

</style>