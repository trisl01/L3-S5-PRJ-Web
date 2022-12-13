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
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
