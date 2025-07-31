<template>
  <section class="bg-white min-h-screen">
    <!-- Hero Section -->
    <HeroSection />

    <!-- Dịch vụ nổi bật -->
    <div class="bg-pink-50 py-16">
      <div class="max-w-6xl mx-auto px-4">
        <h2 class="text-3xl font-semibold text-center text-pink-600 mb-12">
          Dịch vụ nổi bật
        </h2>
        <div class="grid md:grid-cols-3 gap-8">
          <div class="bg-white shadow-lg rounded-lg p-6 text-center">
            <img
              src="images/1.png"
              alt="Nail Design"
              class="rounded mb-4 w-full h-40 object-cover"
            />
            <h3 class="font-semibold text-xl mb-2">Sơn Gel</h3>
            <p class="text-gray-500">
              Độ bền cao, màu sắc đa dạng, giữ được lâu mà vẫn bóng đẹp.
            </p>
          </div>
          <div class="bg-white shadow-lg rounded-lg p-6 text-center">
            <img
              src="images/2.png"
              alt="Nail Design"
              class="rounded mb-4 w-full h-40 object-cover"
            />
            <h3 class="font-semibold text-xl mb-2">Đắp Bột</h3>
            <p class="text-gray-500">
              Tạo độ dài và kiểu dáng theo ý muốn, phù hợp mọi phong cách.
            </p>
          </div>
          <div class="bg-white shadow-lg rounded-lg p-6 text-center">
            <img
              src="images/3.png"
              alt="Nail Design"
              class="rounded mb-4 w-full h-40 object-cover"
            />
            <h3 class="font-semibold text-xl mb-2">Vẽ Nail Art</h3>
            <p class="text-gray-500">
              Thiết kế riêng biệt, thể hiện cá tính và sự độc đáo của bạn.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import HeroSection from "~/components/HeroSection.vue";

// Không cần script cho phần này
</script>
