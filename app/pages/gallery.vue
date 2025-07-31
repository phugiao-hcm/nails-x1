<template>
  <div class="max-w-6xl mx-auto py-12 px-4">
    <h1 class="text-4xl font-bold text-center mb-8 text-pink-600">
      Thư viện hình ảnh
    </h1>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      <img
        v-for="(img, index) in images"
        :key="index"
        :src="img"
        alt="Hình ảnh tiệm nail"
        class="rounded-lg shadow hover:scale-105 transition-transform duration-300"
      />
    </div>
  </div>
</template>

<script setup>
import image1 from "/images/1.png";
import image2 from "/images/2.png";
import image3 from "/images/3.png";
import image4 from "/images/4.png";

const images = [
  image1,
  image2,
  image3,
  image4,
  // thêm ảnh tùy ý
];
</script>
