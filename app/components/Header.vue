<template>
  <header class="bg-pink-500 text-white">
    <div class="container mx-auto flex justify-between items-center p-4">
      <NuxtLink to="/" class="hover:underline"
        ><h1 class="text-2xl font-bold">Tiệm Nails Xinh</h1></NuxtLink
      >
      <!-- Nút toggle menu mobile -->
      <button
        class="md:hidden focus:outline-none"
        @click="isOpen = !isOpen"
        aria-label="Toggle Menu"
      >
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>

      <!-- Menu trên desktop -->
      <nav class="hidden md:flex space-x-6">
        <NuxtLink to="/services" class="hover:underline">Dịch vụ</NuxtLink>
        <NuxtLink to="/pricing" class="hover:underline">Bảng giá</NuxtLink>
        <NuxtLink to="/gallery" class="hover:underline">Hình ảnh</NuxtLink>
        <NuxtLink to="/booking" class="hover:underline">Đặt lịch</NuxtLink>
      </nav>
    </div>

    <!-- Menu mobile -->
    <div v-if="isOpen" class="md:hidden px-4 pb-4 space-y-2">
      <NuxtLink to="/services" class="block hover:underline">Dịch vụ</NuxtLink>
      <NuxtLink to="/pricing" class="block hover:underline">Bảng giá</NuxtLink>
      <NuxtLink to="/gallery" class="block hover:underline">Hình ảnh</NuxtLink>
      <NuxtLink to="/booking" class="block hover:underline">Đặt lịch</NuxtLink>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";
const isOpen = ref(false);
</script>
