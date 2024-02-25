<template>
  <div class="bg-gray-100 min-h-screen py-8">
    <div class="max-w-3xl mx-auto">
      <h1 class="text-3xl font-bold text-center mb-8">News Headlines</h1>
      <ul>
        <li v-for="(article, index) in articles" :key="index" class="bg-white rounded-lg shadow-md p-6 mb-4 hover:shadow-lg transform hover:scale-105 transition duration-300">
          <h2 class="text-xl font-bold">{{ article.title }}</h2>
          <p class="text-gray-700 mt-2">{{ article.description }}</p>
          <p class="mt-4">
            <a :href="article.url" target="_blank" class="text-blue-500 hover:text-blue-700">Read more</a>
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  
  const articles = ref([]);
  
  onMounted(async () => {
    try {
      const response = await fetch('https://newsapi.org/v2/top-headlines?country=us&apiKey=e5bd758a5c804d6590f92aec18b502c4');
      const data = await response.json();
      articles.value = data.articles;
    } catch (error) {
      console.error('Error fetching news:', error);
    }
  });
  </script>
  