<script>
export default {
  name: 'MainAppointment',
  data() {
    return {}
  }
}
</script>
<template>
  <!-- Appointment section -->
  <div class="appointment">
    <div class="info">
      <h2>Make an Appointment</h2>
      <div class="separator"></div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et est aliquam labore consequatur similique ipsam cum.
        Maiores velit sint autem, nulla consequuntur obcaecati eaque ea totam itaque quaerat mollitia ab!</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

.appointment {
  @include flexColumn();
  // flex

  padding: 150px 0;
  line-height: 2em;
  color: #fff;
  // background
  background-color: #fff;
  background-image: url('/images/paralax-bg-tour-facilities.jpg');
  background-repeat: no-repeat;
  background-size: cover;

  .info {
    @include flexColumn();
    gap: 1em;
    // flex

    width: 600px;
    text-align: center;

    &>* {
      margin: 8px 0;
    }

    h2 {
      font-size: 2em;
      font-weight: 400;
    }

    .separator {
      width: 150px;
      height: 1px;
      background-color: #fff;
    }
  }
}
</style>