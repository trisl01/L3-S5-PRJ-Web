<script setup>
  import AppleCardVue from './AppleCard.vue';
  import AppleData from '../assets/json/apple-data.json';
</script>

<template>
  <div class="container">
    <div class="d-flex flex-wrap">
      <AppleCardVue 
        v-for="apple in AppleData" :key="apple.id" :name="apple.name" :price="apple.price" :stock="apple.stock" :description="apple.description" :bestMonths="apple['best-months']" :image="apple.image"
    </div>
  </div>
</template>