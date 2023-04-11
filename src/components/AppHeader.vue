<script>
import HeaderNav from './HeaderNav.vue';
export default {
  name: 'AppHeader',
  data() {
    return {
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
    <!-- import Nav from separate component -->
    <HeaderNav></HeaderNav>
    <div class="container-centered">
      <div class="header-info">
        <h1>
          Caring <span class="life">For Life</span>
        </h1>
        <p>{{ this.paragraph }}</p>
        <button class="btn btn-primary">Learn More</button>
      </div>
    </div>
  </header>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

header {
  background-image: url('/images/header-image-homepage.jpg');
  background-position: center top;
  height: 850px;
  color: white;

  .container-centered {
    height: 100%;
    display: flex;
    align-items: center;

    .header-info {
      display: flex;
      flex-flow: column nowrap;
      align-items: start;
      gap: 1.5em;

      width: 550px;

      h1 {
        font-weight: 100;
        font-size: 3em;

        .life {
          color: $colorPrimary;
        }
      }
    }
  }


}
</style>