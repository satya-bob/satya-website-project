<template>
    <div class="min-h-screen flex flex-col justify-center items-center bg-gray-100">
      <div class="max-w-md p-8 bg-white rounded-lg shadow-lg">
        <h1 class="text-3xl font-bold text-red-600 mb-4">Oops! Something went wrong.</h1>
        <p class="text-gray-700 mb-4">We're sorry, but an error occurred while processing your request.</p>
        <p class="text-gray-700 mb-8">Please try again later or contact support if the problem persists.</p>
        <NuxtLink to="/" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">Go back to Home Page</NuxtLink>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ErrorPage',
  };
  </script>
  
  <style scoped>
  /* Add any additional custom styles here */
  </style>
  