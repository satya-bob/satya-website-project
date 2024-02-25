
import type productCard from './productCard.vue';

import type productCard from './productCard.vue';
<template>
  <div class="product-details bg-gray-100 p-4 rounded-lg shadow-md overflow-hidden">
    <div class="product-image-container h-64">
      <img :src="product.image" alt="Product Image" class="w-full h-full object-cover transition-transform transform hover:scale-105">
    </div>
    <div class="product-info mt-4">
      <h2 class="text-xl font-semibold">{{ product.title }}</h2>
      <h3 class="text-lg text-gray-700">Price: ${{ product.price }}</h3>
      <h3 class="text-lg text-gray-700">ID: {{ product.id }}</h3>
      <p class="text-gray-600">{{ product.description }}</p>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>


