
import type { ProductCard } from '#build/components';

import type { ProductCard } from '#build/components';

import type { ProductCard } from '#build/components';

  
<template>
  <div class="product-item relative overflow-hidden">
    <img :src="product.image" alt="Product Image" class="w-full h-auto transform hover:scale-105 transition duration-300">
    <div class="absolute inset-0 flex items-end justify-center">
      <NuxtLink :to="`/products/${product.id}`" class="text-white bg-black bg-opacity-50 py-2 px-4 border border-white rounded-lg transition duration-300 hover:bg-opacity-75 hover:shadow-md">View Details</NuxtLink>
    </div>
  </div>
</template>
<script setup>
const { product } = defineProps(['product']);
</script>

<style scoped>
.product-item {
  width: 300px; /* Set the width of the product item */
}

.product-item img {
  object-fit: cover; /* Ensure the image covers the entire container */
}

button {
  cursor: pointer;
}
</style>

