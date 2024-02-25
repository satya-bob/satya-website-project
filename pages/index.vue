<template>
  <div class="home-page-container bg-cover bg-center min-h-screen flex justify-center items-center">
    <div class="text-center text-white">
      <h1 class="text-5xl font-bold mb-4 hover:text-blue-500 transition duration-300">Welcome to Our Website!</h1>
      <p class="text-lg mb-8">This is the home page of our website.</p>
      
      <div class="grid grid-cols-1 gap-4 sm:grid-cols-3">
        <NuxtLink to="/posts" class="button">Posts</NuxtLink>
        <NuxtLink to="/weather" class="button">Weather</NuxtLink>
        <NuxtLink to="/products" class="button">Products</NuxtLink>
        <NuxtLink to="/news" class="button">News Feed</NuxtLink>
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

/* Custom button styles */
.button {
  padding: 1rem 2rem;
  border-radius: 0.5rem;
  background-color: #2c5282; /* Dark blue */
  color: white;
  text-decoration: none;
  display: inline-block;
  transition: background-color 0.3s ease, transform 0.3s ease;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Box shadow */
  border: 2px solid #2c5282; /* Border color */
}

.button:hover {
  background-color: #1a365d; /* Darker blue on hover */
  transform: translateY(-2px); /* Move the button slightly upward on hover */
  border-color: #1a365d; /* Darker border color on hover */
}
</style>


