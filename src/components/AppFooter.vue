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
    <!-- Social -->
    <div class="col">
      <img src="/images/medical_logo_1x_dark.png" alt="logo">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolorum ducimus aspernatur eligendi nobis! Doloribus
        tempora fuga non, deleniti blanditiis accusantium perspiciatis eligendi recusandae earum ducimus quia porro. Unde,
        deleniti quasi.</p>
      <hr>
      <a href="#">Lean More About Us</a>
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
        <li v-for="department in this.store.departmentsLinks">{{ department }}</li>
      </ul>
      <button class="btn btn-secondary">View Our Departments</button>
    </div>
  </footer>
</template>
<style lang="scss" scoped></style>