<template>
  <div class="bg-white">
    <div class="max-w-7xl mx-auto py-18 px-4 py-12 sm:px-6 lg:px-8">
      <div class="text-center">
        <h1
          class="
            mt-1
            text-4xl
            font-extrabold
            text-gray-900
            sm:text-5xl
            sm:tracking-tight
            lg:text-6xl
          "
          v-text="title"
        ></h1>
        <p
          class="max-w-xl mt-5 mx-auto text-xl text-gray-500"
          v-text="subtitle"
        ></p>
      </div>
    </div>
  </div>
</template>

<script setup>
import config from "../config";
const { title, subtitle } = config;
</script>
