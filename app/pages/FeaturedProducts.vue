<template>
  <section class="py-12 px-4 bg-gray-50 text-center">
    <h3 class="text-3xl font-bold mb-8">Mẫu hoa nổi bật</h3>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <div
        v-for="item in products"
        :key="item.id"
        class="bg-white rounded-lg shadow hover:shadow-lg transition"
      >
        <img
          :src="item.image"
          alt=""
          class="w-full h-48 object-cover rounded-t"
        />
        <div class="p-4">
          <h4 class="font-semibold text-lg">{{ item.name }}</h4>
          <p class="text-red-600 font-bold mt-2">{{ item.price }}</p>
          <button class="mt-3 bg-pink-500 text-white px-4 py-2 rounded">
            Mua ngay
          </button>
        </div>
      </div>
    </div>
  </section>

  <section class="py-12 px-4 bg-gray-50 text-center">
    <h3 class="text-3xl font-bold mb-8">Mẫu hoa khai trương</h3>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <div
        v-for="item in products"
        :key="item.id"
        class="bg-white rounded-lg shadow hover:shadow-lg transition"
      >
        <img
          :src="item.image"
          alt=""
          class="w-full h-48 object-cover rounded-t"
        />
        <div class="p-4">
          <h4 class="font-semibold text-lg">{{ item.name }}</h4>
          <p class="text-red-600 font-bold mt-2">{{ item.price }}</p>
          <button class="mt-3 bg-pink-500 text-white px-4 py-2 rounded">
            Mua ngay
          </button>
        </div>
      </div>
    </div>
  </section>

  <section class="py-12 px-4 bg-gray-50 text-center">
    <h3 class="text-3xl font-bold mb-8">Mẫu hoa Tình Nhân</h3>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <div
        v-for="item in products"
        :key="item.id"
        class="bg-white rounded-lg shadow hover:shadow-lg transition"
      >
        <img
          :src="item.image"
          alt=""
          class="w-full h-48 object-cover rounded-t"
        />
        <div class="p-4">
          <h4 class="font-semibold text-lg">{{ item.name }}</h4>
          <p class="text-red-600 font-bold mt-2">{{ item.price }}</p>
          <button class="mt-3 bg-pink-500 text-white px-4 py-2 rounded">
            Mua ngay
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const products = [
  {
    id: 1,
    name: "Bó hoa sinh nhật",
    price: "350.000đ",
    image: "/images/product1.jpg",
  },
  {
    id: 2,
    name: "Lan Hồ Điệp",
    price: "1.200.000đ",
    image: "/images/product2.jpg",
  },
  {
    id: 3,
    name: "Kệ khai trương",
    price: "2.800.000đ",
    image: "/images/product3.jpg",
  },
  {
    id: 4,
    name: "Hoa chia buồn",
    price: "950.000đ",
    image: "/images/product4.jpg",
  },
];
</script>
