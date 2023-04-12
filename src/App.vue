<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  data() {
    return {
    };
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  created() {
    addBackToTop({
      diameter: 64,
      backgroundColor: '#3BAFBF',
      textColor: '#fff',
      scrollDuration: 500,
    });
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
</template>

<style lang="scss"></style>
