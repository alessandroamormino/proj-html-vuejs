<script>
import MainDoctors from './MainDoctors.vue';
import MainServices from './MainServices.vue';
import MainWelcome from './MainWelcome.vue';

export default {
  name: "AppMain",
  data() {
    return {};
  },
  components: { MainWelcome, MainDoctors, MainServices }
}
</script>
<template>
  <main>
    <MainWelcome></MainWelcome>
    <MainDoctors></MainDoctors>
    <MainServices></MainServices>
  </main>
</template>
<style lang="scss" scoped></style>