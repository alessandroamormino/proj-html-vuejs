<script>
import { store } from "../store.js";
export default {
  name: 'AppFooter',
  data() {
    return {
      store,
    }
  },
}
</script>
<template>
  <!-- Footer -->
  <footer>
    <div class="footer-top">
      <!-- Social -->
      <div class="col">
        <img src="/images/medical_logo_1x_dark.png" alt="logo">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorum ducimus aspernatur eligendi nobis! Doloribus
          tempora fuga non, deleniti blanditiis accusantium perspiciatis eligendi recusandae earum ducimus quia porro.
          Unde,
          deleniti quasi.</p>
        <div class="separator-long"></div>
        <a id="about-us" href="#">Lean More About Us</a>
        <div class="social">
          <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
          <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
          <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
        </div>
      </div>
      <!-- Information  -->
      <div class="col">
        <h3>Contact Information</h3>
        <div class="separator"></div>
        <div class="location">
          <i class="fa-solid fa-location-dot"></i>
          <span>121 King Street, London United Kingdom</span>
        </div>
        <div class="phone">
          <i class="fa-solid fa-phone-flip"></i>
          <span>1.800.458.558</span>
        </div>
      </div>
      <!-- Departments -->
      <div class="col">
        <h3>Medical Departments</h3>
        <div class="separator"></div>
        <ul>
          <li v-for="department in this.store.departmentsLinks">
            <i class="fa-solid fa-circle-chevron-right"></i>
            {{ department }}
          </li>
        </ul>
        <button class="btn btn-secondary">View Our Departments</button>
      </div>
    </div>
    <div class="footer-bottom">
      &copy; <span>Copyright 2023-2023 | Handmade Landing Page by Alessandro Amormino | All Rights Reserved | Powered by
        me</span>
    </div>
  </footer>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;
@use '../scss/mixin.scss' as *;

footer {
  .footer-top {
    display: flex;
    gap: 2em;
    // flex
    padding: 4em;

    .col {
      flex: 1 1 0px;
      // flex
      font-size: .9em;
      line-height: 2em;

      p {
        padding-top: .5em;
        padding-bottom: 1.5em;
      }

      .separator-long {
        width: 100%;
        height: 2px;
        background-color: $separator-footer;
      }

      #about-us {
        color: $link-footer;
        text-transform: uppercase;
        text-decoration: none;
      }

      .social {
        display: flex;
        gap: .8em;
        // flex
        padding-top: 1.5em;

        a {
          font-size: 2.5em;
        }
      }

      h3 {
        text-transform: uppercase;
        color: $link-footer;
      }

      .separator {
        width: 35px;
        height: 2px;
        background-color: $colorPrimary;

        margin: 1.5em 0;
      }

      .location,
      .phone {
        display: flex;
        align-items: center;
        gap: 1em;
      }

      .location .fa-solid,
      .phone .fa-solid {
        color: $colorPrimary;
        font-size: 1em;
      }

      .location .fa-location-dot {
        font-size: 1.3em;
      }

      ul {
        li {
          display: flex;
          align-items: center;
          gap: .5em;

          .fa-circle-chevron-right {
            color: $colorPrimary;
            font-size: 1.5em;
          }
        }
      }

      .btn-secondary {
        padding: .8em 2.5em;

        margin-top: 2.5em;

        border: 1px solid #000;
        color: #000;
        font-size: 1.1em;
      }
    }
  }

  .footer-bottom {
    padding: 30px 50px;
    font-size: .7em;
    background-color: $light-grey;
    color: grey
  }
}
</style>