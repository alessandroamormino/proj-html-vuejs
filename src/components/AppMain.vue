<script>
import MainDoctors from './MainDoctors.vue';
import MainFacilities from './MainFacilities.vue';
import MainServices from './MainServices.vue';
import MainWelcome from './MainWelcome.vue';

export default {
  name: "AppMain",
  data() {
    return {};
  },
  components: { MainWelcome, MainDoctors, MainServices, MainFacilities }
}
</script>
<template>
  <main>
    <MainWelcome></MainWelcome>
    <MainDoctors></MainDoctors>
    <MainServices></MainServices>
    <MainFacilities></MainFacilities>
  </main>
</template>
<style lang="scss" scoped></style>