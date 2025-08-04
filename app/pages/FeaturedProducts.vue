<template>
    <div>
        <section class="py-12 bg-gray-50 text-center">
            <h3 class="text-3xl font-bold mb-8">Mẫu hoa nổi bật</h3>

            <div class="max-w-7xl mx-auto px-4">
                <Swiper
                    :modules="[Navigation, Pagination]"
                    :slides-per-view="1"
                    :space-between="20"
                    :breakpoints="{
                        640: { slidesPerView: 2 },
                        1024: { slidesPerView: 4 },
                    }"
                    navigation
                    pagination
                    class="pb-10"
                >
                    <SwiperSlide v-for="item in products" :key="item.id">
                        <div
                            class="bg-white rounded-lg shadow hover:shadow-lg transition h-full"
                        >
                            <img
                                :src="item.image"
                                alt=""
                                class="w-full h-48 object-cover rounded-t"
                            />
                            <div class="p-4">
                                <h4 class="font-semibold text-lg">
                                    {{ item.name }}
                                </h4>
                                <p class="text-red-600 font-bold mt-2">
                                    {{ item.price }}
                                </p>
                                <button
                                    class="mt-3 bg-pink-500 text-white px-4 py-2 rounded"
                                >
                                    Mua ngay
                                </button>
                            </div>
                        </div>
                    </SwiperSlide>
                </Swiper>
            </div>
        </section>

        <section class="py-12 bg-gray-50 text-center">
            <h3 class="text-3xl font-bold mb-8">Mẫu Hoa sinh nhật</h3>

            <div class="max-w-7xl mx-auto px-4">
                <Swiper
                    :modules="[Navigation, Pagination]"
                    :slides-per-view="1"
                    :space-between="20"
                    :breakpoints="{
                        640: { slidesPerView: 2 },
                        1024: { slidesPerView: 4 },
                    }"
                    navigation
                    pagination
                    class="pb-10"
                >
                    <SwiperSlide v-for="item in products" :key="item.id">
                        <div
                            class="bg-white rounded-lg shadow hover:shadow-lg transition h-full"
                        >
                            <img
                                :src="item.image"
                                alt=""
                                class="w-full h-48 object-cover rounded-t"
                            />
                            <div class="p-4">
                                <h4 class="font-semibold text-lg">
                                    {{ item.name }}
                                </h4>
                                <p class="text-red-600 font-bold mt-2">
                                    {{ item.price }}
                                </p>
                                <button
                                    class="mt-3 bg-pink-500 text-white px-4 py-2 rounded"
                                >
                                    Mua ngay
                                </button>
                            </div>
                        </div>
                    </SwiperSlide>
                </Swiper>
            </div>
        </section>

        <section class="py-12 bg-gray-50 text-center">
            <h3 class="text-3xl font-bold mb-8">Mẫu Hoa Cắm Bình</h3>

            <div class="max-w-7xl mx-auto px-4">
                <Swiper
                    :modules="[Navigation, Pagination]"
                    :slides-per-view="1"
                    :space-between="20"
                    :breakpoints="{
                        640: { slidesPerView: 2 },
                        1024: { slidesPerView: 4 },
                    }"
                    navigation
                    pagination
                    class="pb-10"
                >
                    <SwiperSlide v-for="item in products" :key="item.id">
                        <div
                            class="bg-white rounded-lg shadow hover:shadow-lg transition h-full"
                        >
                            <img
                                :src="item.image"
                                alt=""
                                class="w-full h-48 object-cover rounded-t"
                            />
                            <div class="p-4">
                                <h4 class="font-semibold text-lg">
                                    {{ item.name }}
                                </h4>
                                <p class="text-red-600 font-bold mt-2">
                                    {{ item.price }}
                                </p>
                                <button
                                    class="mt-3 bg-pink-500 text-white px-4 py-2 rounded"
                                >
                                    Mua ngay
                                </button>
                            </div>
                        </div>
                    </SwiperSlide>
                </Swiper>
            </div>
        </section>
    </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { Navigation, Pagination } from "swiper/modules";

const products = [
    {
        id: 1,
        name: "Bó hoa sinh nhật",
        price: "350.000đ",
        image: "images/hoa_noi_bat_1.png",
    },
    {
        id: 2,
        name: "Lan Hồ Điệp",
        price: "1.200.000đ",
        image: "images/hoa_noi_bat_2.png",
    },
    {
        id: 3,
        name: "Kệ khai trương",
        price: "2.800.000đ",
        image: "images/hoa_noi_bat_3.png",
    },
    {
        id: 4,
        name: "Hoa chia buồn",
        price: "950.000đ",
        image: "images/hoa_noi_bat_4.png",
    },
    {
        id: 5,
        name: "Hoa chia buồn 2",
        price: "950.000đ",
        image: "images/hoa_noi_bat_5.png",
    },
];
</script>
