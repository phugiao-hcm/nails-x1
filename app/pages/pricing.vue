<template>
  <div class="py-20 px-4 bg-white text-center">
    <h1 class="text-4xl md:text-5xl font-bold text-pink-600 mb-6">
      Bảng Giá Dịch Vụ
    </h1>
    <p class="text-gray-600 mb-10 max-w-2xl mx-auto">
      Tham khảo bảng giá các dịch vụ làm móng tại Tiệm Nail Xinh. Chúng tôi luôn
      mang đến chất lượng và trải nghiệm tốt nhất cho bạn!
    </p>

    <div class="max-w-4xl mx-auto grid gap-6 md:grid-cols-2">
      <div
        v-for="(item, index) in services"
        :key="index"
        class="border rounded-xl p-6 shadow hover:shadow-lg transition text-left"
      >
        <div class="flex justify-between items-center mb-2">
          <h2 class="text-xl font-semibold text-gray-800">
            {{ item.name }}
          </h2>
          <span class="text-pink-500 font-bold text-lg">
            {{ item.price }}
          </span>
        </div>
        <p class="text-gray-500 text-sm">{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  {
    name: "Sơn gel tay",
    price: "150.000đ",
    description: "Làm sạch móng, sơn gel cao cấp, bền màu.",
  },
  {
    name: "Sơn gel chân",
    price: "180.000đ",
    description: "Chăm sóc móng chân, sơn gel chất lượng cao.",
  },
  {
    name: "Đắp bột",
    price: "300.000đ",
    description: "Tạo độ dài cho móng bằng bột chuyên nghiệp.",
  },
  {
    name: "Vẽ móng nghệ thuật",
    price: "50.000đ - 200.000đ",
    description: "Thiết kế theo yêu cầu, sáng tạo độc đáo.",
  },
];
</script>
