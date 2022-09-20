<template>
  <div class="bg-video">
    <video
      src="../static/index-about-video.mp4"
      autoplay
      muted
      preload="metadata"
      type="video/mp4"
      loop  
    ></video>
  </div>
</template>
<script>
export default {}
</script>
<style scoped>
.bg-video { 
  position: absolute;
  width: auto;
  height: 100%;
  top: 0px;
  left: -80px;
}
.bg-video video {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
</style>