<script setup>
  defineProps({
    cart: Number
  })
</script>

<template>
  <nav class="bg-white">
    <div class="container">
      <header class="d-flex flex-wrap justify-content-center py-3 mb-4 border-bottom">
        <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto text-dark text-decoration-none">
          <img id="img-logo" src="../assets/logo.png" alt="" srcset="">
          <span id="text-logo" class="fs-4 font-lobster-two"><i class="italic">Pomme</i></span>
        </a>

        <ul class="nav nav-pills">
          <li class="nav-item"><a href="/" class="nav-link">Home</a></li>
          <li class="nav-item"><a href="/" class="nav-link active">Shop</a></li>
          <li class="nav-item"><a href="/" class="btn btn-info">
            <i :class="{ 'bi bi-cart': cart <= 0, 'bi bi-cart-fill': cart > 0 }"></i>
            <span class="ml-10">{{ cart }}</span>
          </a></li>
        </ul>
      </header>
    </div>
  </nav>
</template>

<style scoped>
  nav {
    position: sticky;
    display: block;
    top: 0;
  }
  
  nav li {
    margin-left: 5px;
  }

  .nav-link {
    cursor: pointer;
  }

  #img-logo {
    height: 50px;
  }

  #text-logo {
    font-size: 27px !important;
    font-style: italic !important;
  }
</style>
