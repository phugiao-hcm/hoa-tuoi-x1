<template>
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div
            class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center"
        >
            <!-- Logo -->
            <NuxtLink to="/" class="text-xl font-bold text-gray-900">
                Shop Hoa Xinh
            </NuxtLink>

            <!-- Nút menu mobile -->
            <button
                @click="open = !open"
                class="md:hidden text-gray-800"
                aria-label="Toggle menu"
            >
                <!-- Icon mở -->
                <svg
                    v-if="!open"
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4 6h16M4 12h16M4 18h16"
                    />
                </svg>
                <!-- Icon đóng -->
                <svg
                    v-else
                    class="w-6 h-6"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M6 18L18 6M6 6l12 12"
                    />
                </svg>
            </button>

            <!-- Menu desktop -->
            <nav class="hidden md:flex space-x-6 text-gray-700 font-medium">
                <NuxtLink to="/" class="hover:text-pink-500"
                    >Trang chủ</NuxtLink
                >
                <NuxtLink to="/" class="hover:text-pink-500">Sản phẩm</NuxtLink>
                <NuxtLink to="/" class="hover:text-pink-500">Blog</NuxtLink>
                <NuxtLink to="/" class="hover:text-pink-500"
                    >Giới thiệu</NuxtLink
                >
            </nav>
        </div>

        <!-- Menu mobile -->
        <transition name="fade">
            <div v-if="open" class="md:hidden bg-white px-4 pb-4 space-y-2">
                <NuxtLink to="/" class="block text-gray-700 hover:text-pink-500"
                    >Trang chủ</NuxtLink
                >
                <NuxtLink to="/" class="block text-gray-700 hover:text-pink-500"
                    >Sản phẩm</NuxtLink
                >
                <NuxtLink to="/" class="block text-gray-700 hover:text-pink-500"
                    >Blog</NuxtLink
                >
                <NuxtLink to="/" class="block text-gray-700 hover:text-pink-500"
                    >Giới thiệu</NuxtLink
                >
            </div>
        </transition>
    </header>
</template>

<script setup>
import { ref } from "vue";
const open = ref(false);
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}
</style>
