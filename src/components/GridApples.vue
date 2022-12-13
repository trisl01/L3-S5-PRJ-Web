<script setup>
  import AppleCardVue from './AppleCard.vue';
  import AppleData from '../assets/json/apple-data.json';
</script>

<template>
  <div class="container">
    <h1 class="font-lobster-two">Apple Store</h1>
    <br>
    <p class="font-lobster-two">
      Welcome to the Apple Store! Here you can find all the apples you need to make your favorite apple pie!<br>
      We have a wide variety of apples, from the most common ones to the rarest ones. You can find them all here!<br>
      We have {{ AppleData.length }} different apples in our store!<br>
      Here are some of our best sellers:
    </p>
    <div class="d-flex flex-wrap">
      <AppleCardVue 
        v-for="apple in AppleData" :key="apple.id" :name="apple.name" :price="apple.price" :stock="apple.stock" :description="apple.description" :bestMonths="apple['best-months']" :image="apple.image"
        @add-to-cart="$emit('add-to-cart', 1)"/>
    </div>
  </div>
</template>