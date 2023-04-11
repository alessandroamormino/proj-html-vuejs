<script>
import HeaderNav from './HeaderNav.vue';
export default {
  name: 'AppHeader',
  data() {
    return {
      title: 'Caring For Life',
      paragraph: 'Kind words can be short and easy to speak, but their echoes are truly endless. Avada Health focuses on you as if it was our own family.',
    };
  },
  components: {
    HeaderNav,
  }
}
</script>
<template>
  <header>
    <HeaderNav></HeaderNav>
    <div class="container-centered">
      <h1>{{ this.title }}</h1>
      <p>{{ this.paragraph }}</p>
      <button class="btn btn-primary">Learn More</button>
    </div>
  </header>
</template>
<style lang="scss" scoped>
header {
  background-image: url('/images/header-image-homepage.jpg');
  height: 850px;
}
</style>