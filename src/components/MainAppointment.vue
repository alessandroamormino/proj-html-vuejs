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
  <div id="appointment">
    <div class="info">
      <h2>Make an Appointment</h2>
      <div class="separator"></div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et est aliquam labore consequatur similique ipsam cum.
        Maiores velit sint autem, nulla consequuntur obcaecati eaque ea totam itaque quaerat mollitia ab!</p>
    </div>
    <!-- Form section -->
    <form action="" class="form">
      <div class="row">
        <input type="text" id="name" placeholder="Name*" required>
        <input type="email" id="email" placeholder="Email*" required>
      </div>
      <div class="row">
        <input type="tel" id="phone" placeholder="Phone Number">
        <input type="text" placeholder="Appointment Date" onfocus="(this.type='date')" onblur="(this.type='text')">
      </div>
      <textarea id="message" type="text" placeholder="How can we help?*" rows="4"></textarea>
      <input type="submit" class="btn btn-primary" value="Make an appointment">
    </form>
  </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

#appointment {
  @include flexColumn();
  // flex

  padding: 150px 0;
  line-height: 2em;
  color: #fff;
  // background
  background-color: #fff;
  background-image: url('/images/make-an-appointment.jpg');
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

  .form {
    display: flex;
    flex-flow: column nowrap;
    gap: 2em;
    // flex

    width: 600px;

    .row {
      @include flexCenter();
      gap: 2em;
      // flex
    }

    input,
    textarea {
      flex-grow: 1;
      // flex
      padding: 1em;

      background-color: transparent;
      color: #fff;
      border: 1px solid #fff;

      font-size: .8em;
    }

    .btn-primary {
      border: none;
      background-color: $colorPrimary;

      &:hover {
        background-color: $colorPrimaryHover;
      }
    }
  }
}
</style>