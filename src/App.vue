<template>
  <div id="container">
    <header-top> </header-top>
    <contenu></contenu>
  </div>
</template>

<script>
import Contenu from './components/Contenu/Contenu.vue'
import Header from './components/Header/Header.vue'

export default {
  name: 'App',
  components: {
    'header-top':Header,
    'contenu':Contenu
  }
}
</script>

<style>

</style>
