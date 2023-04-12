<script>
export default {
  name: 'MainFacilities',
  data() {
    return {}
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
      <img src="/images/play-icon.png" alt="Play">
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

.facilities {
  @include flexColumn();
  // flex

  padding: 100px;
  line-height: 2em;

  background-color: #fff;
  background-image: url('/images/paralax-bg-tour-facilities.jpg');

  .info {
    @include flexColumn();
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
}
</style>