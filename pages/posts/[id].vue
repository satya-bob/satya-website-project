<template>
  <div>
    <!-- Check if 'post' is defined -->
    <template v-if="posts">
      <h1>{{ post.title }}</h1>
      <p>{{ post.content }}</p>
      <!-- Other content -->
    </template>
    <!-- If 'post' is not defined, display a loading message -->
    <template v-else>
      <p>Loading...</p>
    </template>
  </div>
</template>

<script>
export default {
  props: ['post'],
}
</script>




  
  <style scoped>
  .bg-gray-100 {
    background-color: #f3f4f6;
  }
  
  .rounded-lg {
    border-radius: 0.5rem;
  }
  
  .shadow-lg {
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }
  
  .hover\:shadow-xl:hover {
    transition: all 0.3s ease;
    box-shadow: 0 8px 12px -4px rgba(0, 0, 0, 0.15), 0 4px 6px -2px rgba(0, 0, 0, 0.1);
  }
  </style>
  