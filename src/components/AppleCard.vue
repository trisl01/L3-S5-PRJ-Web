<script setup>
  defineProps({
    name: String,
    price: String,
    stock: Number,
    description: String,
    bestMonths: String,
    image: String
  })
</script>

<template>
  <div class="container container-apple" style="max-width: 200px;">
    <div class="row">
      <div class="col-12">
        <div class="card" style="min-height: 360px;">
          <div class="card-body d-flex flex-column justify-content-between">
            <div>
              <div style="text-align: center;">
                <img style="width: 100px; height: 100px;" :src="image" :alt="name" />
              </div>
              <div>
                <h5 class="card-title">{{ name }}</h5>
                <h6 class="card-subtitle mb-2 text-muted">{{ price }}</h6>
                <p class="card-text">{{ description }}</p>
                <p class="card-text">{{ bestMonths }}</p>
              </div>
            </div>
            <div class="mt-30" style="text-align: center;">
              <p v-if="stock < 30"
                :class="{ 'text-muted': stock < 30 && stock >= 10, 'text-warning': stock < 10, 'd-none': stock <= 0 }">Almost out of stock! ({{ stock }})</p>
              <button type="button" class="btn btn-primary"
                @click="$emit('add-to-cart', stock--)"
                :disabled="stock <= 0"
                :class="{ 'btn-secondary': stock <= 0 }">
                <i class="bi bi-cart-plus"></i>
                <span class="ml-10">Add to cart</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
  .card-body button .btn-secondary {
    cursor: not-allowed !important;
  }

  .container-apple {
    margin: 10px;
  }
</style>
