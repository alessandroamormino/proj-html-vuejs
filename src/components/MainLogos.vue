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
  <div class="bg">
    <div class="container-centered">
      <div class="logos">
        <div class="slider">
          <img v-for="logo in this.logos" :src="logo" alt="logo">
        </div>
        <div class="slider">
          <img v-for="logo in this.logos" :src="logo" alt="logo">
        </div>
        <div class="slider">
          <img v-for="logo in this.logos" :src="logo" alt="logo">
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@keyframes slide {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-100%);
  }
}

.bg {
  background-image: url('/images/rgb-gradient-bar-for-logo-carrasel.jpg');
  background-repeat: no-repeat;
  background-size: cover;

  .logos {
    overflow: hidden;
    white-space: nowrap;

    &:hover .slider {
      animation-play-state: paused;
      cursor: pointer;
    }

    .slider {
      display: inline-block;
      animation: 10s slide infinite linear;

      img {
        height: 200px;
      }
    }
  }
}
</style>
