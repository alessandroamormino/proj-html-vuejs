<script>
import DoctorsCard from '../components/DoctorsCard.vue';
export default {
  name: 'MainDoctors',
  data() {
    return {
      doctors: [
        {
          name: 'Jon Snow',
          img: '/images/doctor-1.jpg',
          role: 'Anesthesiologist'
        },
        {
          name: 'Tony Stark',
          img: '/images/doctor-2.jpg',
          role: 'Cardiologist'
        },
        {
          name: 'Anna Smith',
          img: '/images/doctor-3.jpg',
          role: 'Nurse Practitioner'
        },
      ],
    }
  },
  components: {
    DoctorsCard
  }
}
</script>
<template>
  <!-- Doctor section -->
  <div class="doctors">
    <!-- info -->
    <div class="info">
      <img src="/images/icon-5.png" alt="Doctors">
      <h2>Meet Our Doctors</h2>
      <div class="separator"></div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et est aliquam labore consequatur similique ipsam cum.
        Maiores velit sint autem, nulla consequuntur obcaecati eaque ea totam itaque quaerat mollitia ab!</p>
    </div>
    <!-- card -->
    <div class="card-container">
      <DoctorsCard v-for="doctor in this.doctors" :doctorCard="doctor"></DoctorsCard>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

.doctors {
  @include flexColumn();
  // flex

  padding: 100px;
  line-height: 2em;

  background-color: $bg-Doctors;

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
      text-transform: uppercase;
      font-weight: 400;
    }

    .separator {
      width: 150px;
      height: 1px;
      background-color: #80808080;
    }
  }

  .card-container {
    @include flexCenter();
    gap: 2em;
    // flex
    padding: 3em 0;
  }
}
</style>