<script setup>
  import { ref } from 'vue'
  import NavbarVue from './components/Navbar.vue'
  import GridApplesVue from './components/GridApples.vue';
  import FooterVue from './components/Footer.vue';
  const cart = ref(0);
</script>

<template>
  <NavbarVue :cart="cart"/>
  <GridApplesVue @add-to-cart="(i) => cart += i"/>
</template>