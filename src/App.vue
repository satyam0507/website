<template>
  <div class="text-center container max-w-lg mx-auto py-12">
    <h1 class="text-3xl mb-6 font-extrabold">{{headline}}</h1>
    <p class="text-xl mb-8 mx-8">{{subtitle}}</p>
    <Links :links="links" />
  </div>
</template>

<script setup>
import Links from './components/Links.vue'

const headline = "Kristian Freeman"
const subtitle = "Developer advocate and software engineer"

const links = [
  {
    name: "Twitter",
    url: "https://twitter.com/signalnerve"
  },
  {
    name: "GitHub",
    url: "https://github.com/signalnerve"
  },
]
</script>

<style>
body {
  background: #1F2937;
  color: #F9FAFB;
}
</style>
