<script>
export default {
  name: 'MainWelcome',
  data() {
    return {
      title: 'Welcome to Avada Health',
      welcomeCards: [
        {
          title: 'Some Day Appointments',
          icon: '/images/icon-1.png'
        },
        {
          title: 'World Class Facilities',
          icon: '/images/icon-2.png'
        },
        {
          title: 'Expert Doctors',
          icon: '/images/icon-3.png'
        },
        {
          title: 'Complementary Therapies',
          icon: '/images/icon-4.png'
        },
      ],
    }
  }
}
</script>
<template>
  <!-- Welcome section -->
  <div class="welcome">
    <div class="info">
      <h2>{{ this.title }}</h2>
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facilis, quasi. Incidunt accusantium hic, tempore quod
        maxime corrupti veritatis deserunt atque illum odit voluptates iure!
      </p>
    </div>
    <div class="container-centered">
      <div v-for="card in welcomeCards" class="card">
        <img :src="card.icon" :alt="card.title">
        <h4>{{ card.title }}</h4>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

.welcome {
  padding: 100px;
  text-align: center;
  line-height: 2em;

  &>* {
    padding: 8px 0;
  }

  .info {
    padding: 0 300px;

    h2 {
      font-size: 2em;
      font-weight: 400;
    }

    p {
      padding: 2em 0;
    }
  }
}

.container-centered {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2em;

  .card {
    width: calc(100% / 4 - 2em / 4 * 3);

    &:hover {
      cursor: pointer;

      h4 {
        color: $colorPrimary;
      }
    }

    h4 {
      font-weight: 400;
      text-transform: uppercase;
    }

    p {
      padding: 1em 0;
      font-size: .9em;
    }
  }
}
</style>