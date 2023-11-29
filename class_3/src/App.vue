<script setup>
const project_title = "Logic in Vue.js";
const location = "Dhaka";
const Weather = "s";

</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">{{ project_title }}</h1>
    <div class="w-1/3 bg-gray-200 p-10 flex items-center flex-col space-y-10">
      <h1 class="text-3xl">{{ location }}</h1>
      <h2 class="text-2xl" v-show=" Weather =='s'"> Weather: Sunny</h2>
      <h2 class="text-2xl" v-show=" Weather =='pc'"> Weather: Partly Cloudy</h2>
      <h2 class="text-2xl" v-show=" Weather =='r'"> Weather: Rainy</h2>
      <h2 class="text-2xl" v-show=" Weather =='t'"> Weather: Thunderstorm </h2>
      <h2 class="text-2xl" v-show=" Weather =='c'"> Weather: Cyclone </h2>
      <img v-if=" Weather =='s'" src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7911203/weather-icon-md.png" alt="sunny">
      <img v-show=" Weather =='pc'" src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912718/weather-icon-md.png" alt="cloudy">
      <img v-show=" Weather =='r'" src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7913380/weather-icon-md.png" alt="rainy">
      <img v-show=" Weather =='t'" src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912589/weather-icon-md.png" alt="thunderstorm">
    </div>
  </section>
</template>

<style scoped>
</style>
