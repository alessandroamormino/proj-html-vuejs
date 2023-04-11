<script>
import MainDoctors from './MainDoctors.vue';
import MainWelcome from './MainWelcome.vue';

export default {
  name: "AppMain",
  data() {
    return {};
  },
  components: { MainWelcome, MainDoctors }
}
</script>
<template>
  <main>
    <!-- Import sections create in components -->
    <MainWelcome></MainWelcome>
    <MainDoctors></MainDoctors>
  </main>
</template>
<style lang="scss" scoped></style>