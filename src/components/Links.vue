<template>
  <div class="flex w-full mb-6" v-for="link in links">
    <a 
      class="text-xl rounded-md py-2 px-4 text-center w-full border border-gray-600 hover:bg-gray-500 transition-all" 
      :href="link.url"
      target="_blank"
    >
      {{link.name}}
    </a>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'
defineProps({ links: Array })
</script>