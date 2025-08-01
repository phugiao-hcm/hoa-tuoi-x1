<template>
  <section class="pt-16 pb-8 px-4 text-center">
    <h3 class="text-3xl font-bold mb-8">Blog hoa mới nhất</h3>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="post in posts"
        :key="post.id"
        class="bg-white rounded-lg shadow hover:shadow-lg transition p-4"
      >
        <img
          :src="post.image"
          alt=""
          class="w-full h-40 object-cover rounded-t"
        />
        <h4 class="mt-3 font-semibold">{{ post.title }}</h4>
      </div>
    </div>
  </section>
</template>

<script setup>
const posts = [
  { id: 1, title: "Ý nghĩa màu sắc hoa hồng", image: "/images/blog1.jpg" },
  { id: 2, title: "Cách giữ hoa lâu tươi", image: "/images/blog2.jpg" },
  { id: 3, title: "Mẫu hoa cưới tuyệt đẹp", image: "/images/blog3.jpg" },
];
</script>
