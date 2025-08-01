<template>
  <transition name="fade">
    <div
      v-if="show"
      class="fixed inset-0 bg-black/60 z-50 flex items-center justify-center"
    >
      <div class="bg-white rounded-lg p-6 max-w-sm w-full relative">
        <button
          @click="show = false"
          class="absolute top-3 right-3 text-gray-500"
        >
          ✕
        </button>
        <h4 class="text-xl font-semibold mb-3">Bạn cần hỗ trợ?</h4>
        <p class="mb-4">Chúng tôi sẵn sàng tư vấn miễn phí 24/7.</p>
        <button class="w-full bg-pink-500 text-white py-2 rounded mb-2">
          Chat Zalo
        </button>
        <button
          class="w-full border border-pink-500 text-pink-500 py-2 rounded"
        >
          Nhắn tin Fanpage
        </button>
      </div>
    </div>
  </transition>
</template>

<script setup>
import { ref, onMounted } from "vue";
const show = ref(false);
onMounted(() => setTimeout(() => (show.value = true), 3000));
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
