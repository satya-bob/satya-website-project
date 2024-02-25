<template>
  <div class="bg-gray-200 min-h-screen flex justify-center items-center">
    <div class="max-w-md bg-white p-8 rounded-lg shadow-md">
      <input type="text" v-model="city" placeholder="Enter a city" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-500">
      <button @click="searchWeather" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600 focus:outline-none focus:bg-blue-600 transition duration-300">Search</button>
      <div v-if="weatherData" class="mt-8">
        <h2 class="text-2xl font-bold">{{ weatherData.name }}</h2>
        <p class="mt-2">Temperature: {{ weatherData.main.temp }}°C</p>
        <p>Weather: {{ weatherData.weather[0].description }}</p>
      </div>
    </div>
  </div>
</template>
  
  <script>
  export default {
    data() {
      return {
        city: '',
        weatherData: null
      };
    },
    methods: {
      async searchWeather() {
        if (this.city.trim() !== '') {
          const apiKey = '48f1792ed1b8cfa3672b4a11f752ab2e';
          const url = `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=${apiKey}&units=metric`;
  
          try {
            const response = await fetch(url);
            if (response.ok) {
              this.weatherData = await response.json();
            } else {
              console.error('Failed to fetch weather data:', response.statusText);
            }
          } catch (error) {
            console.error('Error fetching weather data:', error);
          }
        }
      }
    }
  };
  </script>
  