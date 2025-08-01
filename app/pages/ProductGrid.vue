<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-6xl mx-auto px-4 grid grid-cols-1 md:grid-cols-2 gap-8">
      <div
        v-for="product in products"
        :key="product.title"
        class="bg-white rounded-xl overflow-hidden shadow"
      >
        <img :src="product.image" alt="" class="w-full h-64 object-cover" />
        <div class="p-4">
          <h3 class="text-xl font-semibold mb-2">{{ product.title }}</h3>
          <p class="text-gray-600 mb-4">{{ product.description }}</p>
          <NuxtLink to="#" class="text-blue-500 hover:underline"
            >Tìm hiểu thêm</NuxtLink
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const products = [
  {
    title: "iPhone 14 Pro",
    description: "Camera 48MP. Dynamic Island.",
    image: "/images/8.png",
  },
  {
    title: "iPhone 12",
    description: "Giá dễ tiếp cận. Hiệu năng mạnh mẽ.",
    image: "/images/9.png",
  },
  {
    title: "iPhone 15",
    description: "Giá dễ tiếp cận. Hiệu năng mạnh mẽ.",
    image: "/images/10.png",
  },
  {
    title: "iPhone 16",
    description: "Giá dễ tiếp cận. Hiệu năng mạnh mẽ.",
    image: "/images/11.png",
  },
];
</script>
