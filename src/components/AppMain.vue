<script>
import MainAppointment from './MainAppointment.vue';
import MainDoctors from './MainDoctors.vue';
import MainFacilities from './MainFacilities.vue';
import MainLogos from './MainLogos.vue';
import MainServices from './MainServices.vue';
import MainWelcome from './MainWelcome.vue';

export default {
  name: "AppMain",
  data() {
    return {};
  },
  components: { MainWelcome, MainDoctors, MainServices, MainFacilities, MainAppointment, MainLogos }
}
</script>
<template>
  <main>
    <MainWelcome></MainWelcome>
    <MainDoctors></MainDoctors>
    <MainServices></MainServices>
    <MainFacilities></MainFacilities>
    <MainAppointment></MainAppointment>
    <MainLogos></MainLogos>
  </main>
</template>
<style lang="scss" scoped></style>