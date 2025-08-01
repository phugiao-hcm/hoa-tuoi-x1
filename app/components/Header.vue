<template>
  <header class="bg-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <NuxtLink to="/" class="text-xl font-bold text-gray-900"
        >Shop Hoa Xinh</NuxtLink
      >
      <button @click="open = !open" class="md:hidden">
        <svg v-if="!open" class="w-6 h-6">...</svg>
        <svg v-else class="w-6 h-6">...</svg>
      </button>
      <nav class="hidden md:flex space-x-5">
        <NuxtLink to="/" class="hover:text-pink-500">Trang chủ</NuxtLink>
        <NuxtLink to="/product" class="hover:text-pink-500">Sản phẩm</NuxtLink>
        <NuxtLink to="/blog" class="hover:text-pink-500">Blog</NuxtLink>
        <NuxtLink to="/about" class="hover:text-pink-500">Giới thiệu</NuxtLink>
      </nav>
    </div>
    <div v-if="open" class="md:hidden bg-white px-4 pb-4 space-y-2">
      <NuxtLink to="/" class="block">Trang chủ</NuxtLink>
      <NuxtLink to="/product" class="block">Sản phẩm</NuxtLink>
      <NuxtLink to="/blog" class="block">Blog</NuxtLink>
      <NuxtLink to="/about" class="block">Giới thiệu</NuxtLink>
    </div>
  </header>
</template>
<script setup>
import { ref } from "vue";
const open = ref(false);
</script>
