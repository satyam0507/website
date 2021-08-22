<template>
  <ul role="list" class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
    <li
      v-for="link in social"
      :key="link.url"
      class="
        col-span-1
        bg-white
        md:rounded-lg
        md:shadow
        divide-y divide-gray-200
        hover:bg-gray-50
        focus:z-10
        focus:outline-none
        focus:ring-1 focus:ring-indigo-500
        focus:border-indigo-500
        transition-all
        duration-150
        ease-in-out
      "
    >
      <a v-bind:href="link.url">
        <div class="w-full flex items-center justify-between p-6 space-x-6">
          <img class="w-10 h-10 flex-shrink-0" :src="link.imageUrl" alt="" />
          <div class="flex-1 truncate">
            <div class="flex items-center space-x-3">
              <h3 class="text-gray-900 text-sm font-medium truncate">
                {{ link.title }}
              </h3>
            </div>
          </div>
        </div>
      </a>
    </li>
  </ul>
</template>

<script setup>
import config from "../config";
const { social } = config;
</script>