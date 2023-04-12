<script>
export default {
  name: 'DoctorsCard',
  data() {
    return {}
  },
  props: {
    doctorCard: Object,
  }
}
</script>
<template>
  <!-- import data from component MainDoctor with props -->
  <div class="card">
    <div class="top">
      <img :src="doctorCard.img" :alt="doctorCard.name">
    </div>
    <div class="bottom">
      <span id="doctor-name">{{ doctorCard.name }}</span>
      <span id="role">{{ doctorCard.role }}</span>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit suscipit vel illum sunt.</p>
      <!-- Social Section -->
      <div class="socials">
        <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
        <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
        <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.card {

  .top {
    width: 300px;
    height: 300px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: inline-block;
    }
  }

  .bottom {
    display: flex;
    flex-flow: column nowrap;
    // flex

    width: 300px;
    height: 300px;
    padding: 2em;
    background-color: #fff;

    #doctor-name {
      text-transform: uppercase;
    }

    p {
      font-size: .9em;
      padding: 1.5em 0;
    }

    .socials {
      display: flex;
      gap: .5em;

      .fa-brands {
        font-size: 2em;
      }
    }
  }

  transition: all .4s ease;

  &:hover {
    transform: scale(1.1);
    -webkit-box-shadow: 1px 1px 10px 1px rgba(0, 0, 0, 0.3);
    box-shadow: 1px 1px 10px 1px rgba(0, 0, 0, 0.3);
  }
}
</style>