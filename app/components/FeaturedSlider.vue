<template>
  <div class="w-full">
    <swiper
      :modules="[Navigation, Autoplay, Pagination]"
      :slides-per-view="1"
      :loop="true"
      :autoplay="{ delay: 3000 }"
      :pagination="{ clickable: true }"
      :navigation="true"
      class="aspect-[16/9] sm:aspect-[4/3] md:aspect-[3/2] lg:aspect-[16/6]"
    >
      <swiper-slide
        v-for="(product, index) in products"
        :key="index"
        class="relative w-full h-full"
      >
        <NuxtLink :to="`/products/${index}`" class="block w-full h-full">
          <img
            :src="product.image"
            alt=""
            class="w-full h-full object-contain sm:object-cover object-center transition-all duration-300"
          />
        </NuxtLink>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

const products = [
  {
    name: "Kem Dưỡng Ẩm Ban Đêm",
    image:
      "https://marketplace.canva.com/EAGXkm-nzvU/2/0/1600w/canva-3FOrHNKAiBM.jpg",
    description: "Giữ ẩm chuyên sâu, phù hợp cho mọi loại da.",
    price: "350.000₫",
  },
  {
    name: "Serum Vitamin C",
    image:
      "https://marketplace.canva.com/EAGd9lucSeA/1/0/1600w/canva-z2hiW3pHcYw.jpg",
    description: "Làm sáng da, mờ thâm nám.",
    price: "490.000₫",
  },
  {
    name: "Sữa Rửa Mặt Tạo Bọt",
    image:
      "https://marketplace.canva.com/EAGqnfxyabw/1/0/1600w/canva-3C3nsXC6bVc.jpg",
    description: "Làm sạch nhẹ nhàng, không gây khô da.",
    price: "220.000₫",
  },
];
</script>

<style scoped>
.swiper-button-prev,
.swiper-button-next {
  color: white; /* hoặc dùng Tailwind thêm vào global */
  fill: white !important;
}
</style>
