<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import Benefits from "./components/Benefits.vue";
import Features from "./components/Features.vue";
</script>

<template>
  <Navbar />
  <Hero />
  <Benefits />
  <Features />

  <div class="flex flex-col items-center justify-center pt-12">
    <h2 class="text-center text-2xl text-muted-foreground pb-24">
      New sections in progress...
    </h2>
    <a
      href="https://github.com/leomirandaa"
      target="_blank"
      class="text-sm pb-8 underline"
      >Made by Leo Miranda</a
    >
  </div>
</template>
