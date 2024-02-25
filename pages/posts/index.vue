<template>
  <div class="bg-gray-100 min-h-screen flex justify-center items-center">
    <div class="max-w-md bg-white p-6 rounded-lg shadow-md">
      <h2 class="text-2xl font-bold mb-4">Posts</h2>
      <ul>
        <li v-for="post in posts" :key="post.id" class="mb-4">
          <nuxt-link :to="`posts/${post.id}`" class="block py-2 px-4 rounded-md bg-blue-500 text-white hover:bg-blue-600 transition duration-300 transform hover:scale-105">{{ post.title }}</nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts:  [
    { id: 1, title: 'Introduction to Vue.js', content: 'Vue.js is a progressive JavaScript framework for building user interfaces. It is designed from the ground up to be incrementally adoptable, making it easy to integrate into existing projects.' },
    { id: 2, title: 'Getting Started with Nuxt.js', content: 'Nuxt.js is a powerful framework for building server-side rendered (SSR) Vue.js applications. It provides a lot of built-in features and conventions to streamline development and make SSR setup easy.' },
    { id: 3, title: 'Responsive Web Design Basics', content: 'Responsive web design is an approach to web design that makes web pages render well on a variety of devices and window or screen sizes. It aims to provide an optimal viewing experience across a wide range of devices, from desktop computers to mobile phones.' },
    { id: 4, title: 'CSS Flexbox Layout', content: 'Flexbox is a layout model in CSS that provides a more efficient way to lay out, align, and distribute space among items in a container, even when their size is unknown or dynamic.' },
    { id: 5, title: 'JavaScript Promises Explained', content: 'Promises in JavaScript are objects that represent the eventual completion or failure of an asynchronous operation. They provide a cleaner and more flexible alternative to callback-based asynchronous code.' },
    { id: 6, title: 'Introduction to Node.js', content: 'Node.js is a runtime environment that allows you to run JavaScript code on the server-side. It is built on the V8 JavaScript engine and provides a powerful set of features for building scalable and efficient web applications.' },
    { id: 7, title: 'Using Git for Version Control', content: 'Git is a distributed version control system that allows multiple developers to collaborate on projects and track changes to code over time. It provides powerful branching and merging capabilities, making it easy to manage complex development workflows.' },
    { id: 8, title: 'Vue.js Components and Props', content: 'Components are reusable Vue instances that encapsulate HTML, CSS, and JavaScript code for a specific UI element. Props are custom attributes that can be passed to a component, allowing it to accept data from its parent component.' },
    { id: 9, title: 'Handling Forms in Vue.js', content: 'Vue.js provides built-in features and directives for handling forms, such as `v-model` for two-way data binding and `v-on` for event handling. It also supports form validation and submission using various techniques.' },
    { id: 10, title: 'Optimizing Performance in Vue.js Apps', content: 'Optimizing performance in Vue.js apps involves techniques such as code splitting, lazy loading, caching, and optimizing rendering performance. By implementing these techniques, you can ensure that your Vue.js apps are fast and responsive.' },
    { id: 11, title: 'Using Vuex for State Management', content: 'Vuex is a state management pattern and library for Vue.js applications. It provides a centralized store for managing application state and enables you to easily manage and update state across components.' },
    { id: 12, title: 'Authentication with JWT in Nuxt.js', content: 'JSON Web Tokens (JWT) are a popular method for implementing authentication in web applications. In Nuxt.js, you can use JWT for token-based authentication by integrating libraries such as `@nuxtjs/auth-next`.' },
    { id: 13, title: 'Building RESTful APIs with Express.js', content: 'Express.js is a minimalist web framework for Node.js that provides a set of features for building web applications and APIs. You can use Express.js to create RESTful APIs for your Vue.js or Nuxt.js applications.' },
    { id: 14, title: 'Introduction to MongoDB', content: 'MongoDB is a popular NoSQL database that stores data in flexible, JSON-like documents. It is widely used in modern web development for its scalability, flexibility, and ease of use.' },
    { id: 15, title: 'Deploying Nuxt.js Apps to Production', content: 'Deploying Nuxt.js apps to production involves steps such as building the app for production, configuring the server environment, setting up a reverse proxy, and configuring DNS settings. You can deploy Nuxt.js apps to various platforms, including Heroku, Vercel, and AWS.' }
  ]
    };
  }
}
</script>

  
  <style scoped>
  /* Set full background color */
  body {
    background-color: #f7fafc; /* You can adjust the color as needed */
  }
  </style>
  