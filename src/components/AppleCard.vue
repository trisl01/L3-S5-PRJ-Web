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
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
