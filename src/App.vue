<template>
  <Header />
  <main class="w-full h-full min-h-[calc(100vh-64px)] mt-[64px] flex flex-col items-center justify-center bg-gray-100 p-[1rem]">
    <router-view />
  </main>
</template>

<script setup>
import { RouterView } from 'vue-router';
import Header from '@/components/Header.vue';
</script>