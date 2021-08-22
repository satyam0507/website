<template>
  <Header />
  <div class="max-w-3xl mx-auto">
    <Social />
    <Links />
  </div>

  <Footer />
</template>

<script setup>
import Header from "./components/Header.vue";
import Links from "./components/Links.vue";
import Social from "./components/Social.vue";
import Footer from "./components/Footer.vue";
</script>

<style>
body {
  background: #fefefe;
  color: #1f2937;
}
</style>
