<template>
    <div class="bg-gray-100 h-screen flex justify-center items-center">
      <ProductDetails :product="product" />
    </div>
  </template>
  
  <script setup>
  import { useRoute } from 'vue-router';
 
  
  const { id } = useRoute().params;
  const uri = 'https://fakestoreapi.com/products/' + id;
  
  const { data: product } = await useFetch(uri);
  </script>
  
  <style scoped>
  /* Full-page background color */
  html, body {
    height: 100%;
  }
  
  /* Product card container */
  .product-details {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  /* Hover effect on product details */
  .product-details:hover {
    transform: scale(1.05);
  }
  
  /* Transition effect */
  .product-details {
    transition: transform 0.3s ease;
  }
  </style>
  