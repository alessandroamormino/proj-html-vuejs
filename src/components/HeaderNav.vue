<script>
import { store } from "../store.js";
export default {
  name: 'HeaderNav',
  data() {
    return {
      store,
      isDropdownVisible: false,
    };
  },
}
</script>
<template>
  <nav>
    <div class="nav-right">
      <div class="logo-container">
        <img src="/images/medical_logo_1x_light.png" alt="medical_logo">
      </div>
    </div>
    <div class="nav-left">
      <ul>
        <li><a href="#" class="active">Home</a></li>
        <li><a href="#">About</a></li>
        <li @mouseover="this.isDropdownVisible = true" @mouseleave="this.isDropdownVisible = false">
          <a href="#">
            Departments
            <i v-show="this.isDropdownVisible" class="fas fa-angle-down"></i>
          </a>
          <div v-show="this.isDropdownVisible" class="dropdown">
            <ul class="dropdown-links">
              <li v-for="DepLink in this.store.DepartmentsLinks"><a href="#">{{ DepLink }}</a></li>
            </ul>
          </div>
        </li>
        <li><a href="#">Articles</a></li>
        <li><button class="btn btn-primary">Make Appointments</button></li>
      </ul>
    </div>
  </nav>
</template>
<style lang="scss" scoped>
@use '../scss/mixin.scss' as *;
@use '../scss/variables.scss' as *;


nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100px;
  // position
  padding: 0 5em;
  @include flexRowBetween();

  .nav-left {
    ul:not(.dropdown-links) {
      @include flexRowBetween();
      gap: 3em;

      li {
        color: white;
        text-transform: uppercase;
        font-size: .9em;

        &:nth-child(3) {
          position: relative;
        }

        a {
          color: white;
          text-decoration: none;

          &:hover {
            color: $colorPrimary;
          }
        }

        .active {
          color: $colorPrimary;
        }
      }
    }

    .dropdown {
      position: absolute;
      top: 2em;
      left: 0;
      // position

      background-color: #fff;
      padding: 1em 1.5em;
      width: 250px;

      ul {
        li {
          font-size: 1em;
          padding: 1em 0;
          text-transform: none;

          a {
            color: #000;
            text-decoration: none;
          }
        }
      }
    }
  }
}
</style>