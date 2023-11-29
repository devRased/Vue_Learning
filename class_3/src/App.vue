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
            
            <!-- make it group using div but div is shown on html murkup so we can use template tag which is support only vue.js but dont show in html murkup -->
            <template v-if="Weather=='s'">
                <h2 class="text-2xl" v-if="Weather == 's'">Weather: Sunny</h2>
                <img
                    v-if="Weather == 's'"
                    src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7911203/weather-icon-md.png"
                    alt="sunny"
                />
            </template>
            <template v-if="Weather=='pc'">
                <h2 class="text-2xl">Weather: Partly Cloudy</h2>
                <img
                    src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912718/weather-icon-md.png"
                    alt="cloudy"
                />
            </template>
            <template v-if="Weather=='r'">
                <h2 class="text-2xl">Weather: Rainy</h2>
                <img
                    src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7913380/weather-icon-md.png"
                    alt="rainy"
                />
            </template>
            <template v-if="Weather=='t'">
                <h2 class="text-2xl">Weather: Thunderstorm</h2>
                <img
                    src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7912589/weather-icon-md.png"
                    alt="thunderstorm"
                />
            </template>
        </div>
    </section>
</template>

<style scoped></style>
