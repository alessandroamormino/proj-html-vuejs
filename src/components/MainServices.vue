<script>
export default {
  name: 'MainServices',
  data() {
    return {
      services: [
        {
          title: 'Rehabilitation Center',
          img: '/images/icon-14.png'
        },
        {
          title: 'Dental Implants',
          img: '/images/icon-15.png'
        },
        {
          title: 'Medicine Research',
          img: '/images/icon-16.png'
        },
        {
          title: 'Bload Bank',
          img: '/images/icon-11.png'
        },
        {
          title: 'Pharmaceutical Advice',
          img: '/images/icon-12.png'
        },
        {
          title: 'Medical Counseling',
          img: '/images/icon-13.png'
        },
      ],
    }
  }
}
</script>
<template>
  <!-- Services section -->
  <div class="services">
    <!-- info -->
    <div class="info">
      <img src="/images/icon-6.png" alt="Services">
      <h2>Out Health Services</h2>
      <div class="separator"></div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et est aliquam labore consequatur similique ipsam cum.
        Maiores velit sint autem, nulla consequuntur obcaecati eaque ea totam itaque quaerat mollitia ab!</p>
    </div>
    <div class="container-centered">
      <div v-for="service in this.services" class="card">
        <img :src="service.img" :alt="service.title">
        <span id="title">{{ service.title }}</span>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Exercitationem beatae saepe rerum molestiae amet?
          Quisquam quod saepe, mollitia sunt voluptatem!</p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

.services {
  @include flexColumn();
  // flex

  padding: 100px;
  line-height: 2em;

  background-color: #fff;

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

  .container-centered {
    display: flex;
    flex-flow: row wrap;
    gap: 2em;
    // flex

    padding-top: 80px;

    .card {
      @include flexColumn();
      // flex
      padding-bottom: 60px;
      text-align: center;
      width: calc(100% / 3 - 2em / 3 * 2);

      img {
        width: 70px;
      }

      #title {
        text-transform: uppercase;
        padding: .5em 0;
      }

      p {
        font-size: .9em;
      }

      &:hover {
        cursor: pointer;

        #title {
          color: $colorPrimary;
        }
      }


    }
  }
}
</style>