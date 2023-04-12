<script>
export default {
  name: 'MainFacilities',
  data() {
    return {
      facilities: [
        'Emergency Care',
        'Expert Diagnostics',
        'Superb Rehabilitation'
      ],
    }
  }
}
</script>
<template>
  <!-- Facilities section -->
  <div class="facilities">
    <!-- info -->
    <div class="info">
      <img src="/images/icon-7.png" alt="Facilities">
      <h2>Tour Our Facilities</h2>
      <div class="separator"></div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et est aliquam labore consequatur similique ipsam cum.
        Maiores velit sint autem, nulla consequuntur obcaecati eaque ea totam itaque quaerat mollitia ab!</p>
      <img id="play" src="/images/play-icon.png" alt="Play">
    </div>
  </div>
  <div class="card-container">
    <div v-for="facility in facilities" class="card">
      <span id="facility-name">{{ facility }}</span>
      <img src="/images/wave-divider.png" alt="Divider">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae ratione iusto cumque molestias!.</p>
      <button class="btn btn-secondary">Learn More</button>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

.facilities {
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
      text-transform: uppercase;
      font-weight: 400;
    }

    .separator {
      width: 150px;
      height: 1px;
      background-color: #fff;
    }

    #play {
      transition: transform .4s ease;

      &:hover {
        transform: scale(1.2);
        cursor: pointer;
      }
    }

  }
}

.card-container {
  display: flex;
  align-items: center;
  // flex
  color: #fff;

  .card {
    @include flexColumn();
    flex-grow: 1;
    // flex

    gap: .8em;

    padding: 2.5em 1em;
    text-align: center;

    &:nth-child(1) {
      background-color: $colorPrimary;

      .btn-secondary:hover {
        background-color: #fff;
        color: $colorPrimary;

      }
    }

    &:nth-child(2) {
      background-color: $colorSecondary;

      .btn-secondary:hover {
        background-color: #fff;
        color: $colorSecondary;

      }
    }

    &:nth-child(3) {
      background-color: $colorPrimaryHover;

      .btn-secondary:hover {
        background-color: #fff;
        color: $colorPrimaryHover;

      }
    }


  }
}
</style>