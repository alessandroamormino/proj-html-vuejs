<script>
export default {
  name: 'MainLogos',
  data() {
    return {
      logos: [
        '/images/client-logos-1.png',
        '/images/client-logos-2.png',
        '/images/client-logos-3.png',
        '/images/client-logos-4.png',
      ],
    }
  }
}
</script>
<template>
  <!-- Slider Logos section -->
  <div class="logos">
    <div class="slider container-centered">
      <img v-for="logo in this.logos" :src="logo" alt="logo">
    </div>
  </div>
</template>
<style lang="scss" scoped>
.logos {
  background-image: url('/images/rgb-gradient-bar-for-logo-carrasel.jpg');
  background-repeat: no-repeat;
  background-size: cover;

  .slider {
    img {
      height: 200px;
    }
  }
}
</style>
