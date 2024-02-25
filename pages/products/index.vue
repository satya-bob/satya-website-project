<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
    <div v-for="p in products" :key="p.id" class="relative overflow-hidden rounded-lg shadow-lg">
      <ProductCard :product="p" />
      <div class="absolute inset-0 bg-black bg-opacity-50 opacity-0 hover:opacity-100 transition-opacity duration-300"></div>
      <div class="absolute inset-0 flex items-center justify-center text-white opacity-0 hover:opacity-100 transition-opacity duration-300">
        <div class="text-center">
          <h2 class="text-lg font-semibold">{{ p.title }}</h2>
          <p class="text-sm">{{ p.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Customize hover and transformation effects */
.grid > div:hover .shadow-lg {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.grid > div:hover .hover\:scale-105 {
  transform: scale(1.05);
}

.grid > div:hover .opacity-0 {
  opacity: 0;
}
</style>

  
  <script setup>
  const { data: products } = await useFetch('https://fakestoreapi.com/products');
  </script>
  