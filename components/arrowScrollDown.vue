<template>
  <div class="arrow-scroll-down flex items-center justify-center">
    <v-icon color="white" x-large class="mb-8"> mdi-chevron-down </v-icon>
  </div>
</template>
<script>
export default {}
</script>
<style>
.arrow-scroll-down {
  position: relative;
  height: 80%;
  width: 100%;
  background-color: #009a67;
  z-index: 10000;
  cursor: pointer;
  overflow: hidden;
  -webkit-transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: opacity 0.5s ease, -webkit-transform 0.5s ease;
  transition: transform 0.5s ease, opacity 0.5s ease;
  transition: transform 0.5s ease, opacity 0.5s ease,
    -webkit-transform 0.5s ease;
}
.arrow-scroll-down::after{
  content: '';
  position: absolute;
  top: 100%;
  left: 0;
  opacity: 1;
  background-color: aqua;
  width: 100%;
  height: 100%;
}
.arrow-scroll-down:hover ::after{
  top: 0%;
  left: 0%;
}
</style>