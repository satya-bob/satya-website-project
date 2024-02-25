<template>
  <div>
    <header class="header bg-blue-500 py-4 hover:bg-blue-600 transition duration-300">
      <nav class="nav flex justify-center">
        <NuxtLink to="/" class="nav-link text-white font-bold text-xl hover:text-yellow-400 transition duration-300 transform hover:scale-105">Satya Website</NuxtLink>
      </nav>
    </header>
    <div class="content bg-gray-100 px-4 py-8">
      <slot />
    </div>
    <footer class="footer bg-blue-500 py-4 hover:bg-blue-600 transition duration-300">
      <ul class="footer-links flex justify-center">
        <li><NuxtLink to="/" class="footer-link text-white hover:text-yellow-400 transition duration-300 transform hover:scale-105">Home</NuxtLink></li>
        <li class="ml-4"><NuxtLink to="/about" class="footer-link text-white hover:text-yellow-400 transition duration-300 transform hover:scale-105">About</NuxtLink></li>
        <li class="ml-4"><NuxtLink to="/contact" class="footer-link text-white hover:text-yellow-400 transition duration-300 transform hover:scale-105">Contact Us</NuxtLink></li>
      </ul>
    </footer>
  </div>
</template>

<style scoped>
.header:hover {
  background-color: #3182ce;
}

.footer:hover {
  background-color: #3182ce;
}
</style>
