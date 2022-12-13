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
        <div class="card" style="min-height: 350px;">
          <div class="card-body d-flex flex-column justify-content-between">
              <div style="text-align: center;">
                <img style="width: 100px; height: 100px;" :src="image" :alt="name" />
              </div>
              <div>
                <h5 class="card-title">{{ name }}</h5>
                <h6 class="card-subtitle mb-2 text-muted">{{ price }}</h6>
                <p class="card-text">{{ description }}</p>
                <p class="card-text">{{ bestMonths }}</p>
              </div>
              <button type="button" class="btn btn-primary"
                @click="$emit('add-to-cart', stock--)"
              </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
