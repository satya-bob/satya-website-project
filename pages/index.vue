<template>
  <div class="home-page-container bg-cover bg-center min-h-screen flex justify-center items-center">
    <div class="text-center text-white">
      <h1 class="text-5xl font-bold mb-4 hover:text-blue-500 transition duration-300">Welcome to Our Website!</h1>
      <p class="text-lg mb-8">This is the home page of our website.</p>
      
      <div class="grid grid-cols-1 gap-4 sm:grid-cols-3">
        <NuxtLink to="/posts" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">Posts</NuxtLink>
        <NuxtLink to="/weather" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">Weather</NuxtLink>
        <NuxtLink to="/products" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">Products</NuxtLink>
        <NuxtLink to="/news" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">News Feed</NuxtLink>
      </div>
    </div>
  </div>
</template>

<style scoped>
.home-page-container {
  background-color: #cffafe; /* Semi-transparent black overlay for better text readability */
}

h1,p{
  color:#34d399;
}
/* Styles for hover effects on links */
.home-page-container a:hover {
  transform: translateY(-2px); /* Move the link slightly upward on hover */
}


</style>


