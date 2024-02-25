<template>
    <div class="contact-page-container bg-gray-100 min-h-screen flex justify-center items-center">
      <div class="bg-white p-8 rounded-lg shadow-md">
        <h1 class="text-3xl font-bold mb-6">Contact Us</h1>
        <form @submit.prevent="submitReview" class="space-y-4">
          <div>
            <label for="name" class="block text-gray-700 font-bold">Name:</label>
            <input type="text" id="name" v-model="name" placeholder="Enter your name" class="form-input mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring focus:ring-blue-500 focus:ring-opacity-50">
          </div>
          <div>
            <label for="email" class="block text-gray-700 font-bold">Email:</label>
            <input type="email" id="email" v-model="email" placeholder="Enter your email" class="form-input mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring focus:ring-blue-500 focus:ring-opacity-50">
          </div>
          <div>
            <label for="review" class="block text-gray-700 font-bold">Review:</label>
            <textarea id="review" v-model="review" placeholder="Write your review" class="form-textarea mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring focus:ring-blue-500 focus:ring-opacity-50"></textarea>
          </div>
          <button type="submit" class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 transition duration-300">Submit</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        review: ''
      };
    },
    methods: {
      submitReview() {
        // Here you can submit the review data to your backend or perform any other actions
        console.log('Submitted review:', {
          name: this.name,
          email: this.email,
          review: this.review
        });
        // Clear form fields after submission
        this.name = '';
        this.email = '';
        this.review = '';
      }
    }
  }
  </script>
  
  <style scoped>
  .contact-page-container {
    background-color: #f3f4f6;
  }
  
  /* Styles for form inputs */
  .form-input {
    padding: 0.5rem;
  }
  
  .form-textarea {
    padding: 0.5rem;
    min-height: 120px; /* Set minimum height for textarea */
  }
  </style>
  