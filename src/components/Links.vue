<template>
  <div class="max-w-7xl mx-auto py-18 py-12">
    <ul role="list" class="grid grid-cols-1 gap-6">
      <li
        v-for="link in links"
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
            <div class="flex-1">
              <div class="flex items-center space-x-5">
                <img
                  class="w-14 h-14 flex-shrink-0"
                  v-bind:src="'//logo.clearbit.com/' + baseUrl(link.url)"
                />
                <div>
                  <h3 class="text-gray-900 text-lg font-semibold pb-2">
                    {{ link.title }}
                  </h3>
                  <p class="text-gray-700 text-md">
                    {{ link.subtitle }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script setup>
import config from "../config";
const { links } = config;
const baseUrl = (url) => new URL(url).hostname;
</script>