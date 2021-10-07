<template>
  <div class="header-top">
    <h1>{{ titre }}</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      titre: "La coloc",
    };
  },
};
</script>

<style scoped src='./Header.css'></style>