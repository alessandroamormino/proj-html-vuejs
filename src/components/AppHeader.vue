<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      title: 'Caring For Life',
      paragraph: 'Kind words can be short and easy to speak, but their echoes are truly endless. Avada Health focuses on you as if it was our own family.',
    };
  }
}
</script>
<template>
  nav
  <header>
    <div class="container-centered">
      <h1>{{ this.title }}</h1>
      <p>{{ this.paragraph }}</p>
      <button class="btn btn-primary">Learn More</button>
    </div>
  </header>
</template>
<style lang="scss" scoped></style>