<template>
  <footer class="bg-white">
    <div
      class="
        max-w-7xl
        mx-auto
        py-12
        px-4
        sm:px-6
        md:flex
        md:items-center
        md:justify-between
        lg:px-8
      "
    >
      <div class="flex justify-center space-x-6 md:order-2">
        <a
          v-for="item in social"
          :key="item.url"
          :href="item.url"
          class="text-gray-400 hover:text-gray-500"
        >
          <span class="sr-only">{{ item.title }}</span>
          <img
            class="
              opacity-50
              focus:opacity-100
              hover:opacity-100
              w-4
              h-4
              flex-shrink-0
              transition-all
              duration-150
              ease-in-out
            "
            :src="item.imageUrl"
            alt=""
          />
        </a>
      </div>
      <div class="mt-8 md:mt-0 md:order-1">
        <p class="text-center text-base text-gray-400">
          This project is forked from
          <a
            class="
              underline
              hover:text-gray-600
              focus:text-gray-600
              transition-all
              duration-150
              ease-in-out
            "
            href="https://github.com/signalnerve/signalnerve.com"
            >Kristian's</a
          >.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import config from "../config";
const { social } = config;
</script>