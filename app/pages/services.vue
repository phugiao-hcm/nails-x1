<template>
  <section class="py-16 px-4 max-w-6xl mx-auto">
    <h1 class="text-3xl md:text-4xl font-bold text-center text-pink-600 mb-10">
      Dịch vụ của chúng tôi
    </h1>

    <div class="grid md:grid-cols-3 gap-8">
      <div
        v-for="(service, index) in services"
        :key="index"
        class="bg-white rounded-lg shadow-md p-6 text-center border hover:shadow-lg transition"
      >
        <img
          :src="service.image"
          :alt="service.title"
          class="mx-auto w-24 h-24 object-cover mb-4 rounded-full border border-pink-400"
        />
        <h2 class="text-xl font-semibold mb-2 text-pink-600">
          {{ service.title }}
        </h2>
        <p class="text-gray-600">{{ service.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import image1 from "/images/1.png";
import image2 from "/images/2.png";
import image3 from "/images/3.png";
import image4 from "/images/4.png";

const services = [
  {
    title: "Sơn gel",
    description: "Bền màu, bóng đẹp, giữ màu từ 2-3 tuần.",
    image: image1,
  },
  {
    title: "Đắp bột",
    description: "Tạo dáng móng dài, chắc chắn và nổi bật.",
    image: image2,
  },
  {
    title: "Nail art",
    description: "Trang trí móng tay với họa tiết độc đáo và sáng tạo.",
    image: image3,
  },
  {
    title: "Chăm sóc móng",
    description: "Cắt da, dưỡng móng, chăm sóc tổng thể.",
    image: image3,
  },
  {
    title: "Làm móng chân",
    description: "Sạch sẽ, thư giãn, an toàn với dụng cụ riêng.",
    image: image4,
  },
  {
    title: "Dịch vụ combo",
    description: "Tiết kiệm hơn khi làm combo tay & chân.",
    image: image1,
  },
];
</script>

<style scoped>
/* Nếu muốn thêm tùy biến */
</style>
