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
const images = [
  "images/1.png",
  "images/2.png",
  "images/3.png",
  // thêm ảnh tùy ý
];
</script>
