<template>
  <div class="max-w-xl mx-auto py-10 px-4">
    <h1 class="text-3xl font-bold text-center text-pink-600 mb-6">
      Đặt lịch hẹn
    </h1>

    <form
      @submit.prevent="submitBooking"
      class="space-y-4 bg-white p-6 rounded-xl shadow-lg"
    >
      <div>
        <label class="block mb-1 font-medium text-gray-700">Họ và tên</label>
        <input
          v-model="form.name"
          type="text"
          required
          class="w-full border border-gray-300 p-2 rounded"
        />
      </div>

      <div>
        <label class="block mb-1 font-medium text-gray-700"
          >Số điện thoại</label
        >
        <input
          v-model="form.phone"
          type="tel"
          required
          class="w-full border border-gray-300 p-2 rounded"
        />
      </div>

      <div>
        <label class="block mb-1 font-medium text-gray-700">Ngày hẹn</label>
        <input
          v-model="form.date"
          type="date"
          required
          class="w-full border border-gray-300 p-2 rounded"
        />
      </div>

      <div>
        <label class="block mb-1 font-medium text-gray-700">Giờ hẹn</label>
        <input
          v-model="form.time"
          type="time"
          required
          class="w-full border border-gray-300 p-2 rounded"
        />
      </div>

      <div>
        <label class="block mb-1 font-medium text-gray-700">Ghi chú</label>
        <textarea
          v-model="form.note"
          rows="3"
          class="w-full border border-gray-300 p-2 rounded"
        ></textarea>
      </div>

      <button
        type="submit"
        class="w-full bg-pink-600 text-white py-2 rounded hover:bg-pink-700 transition"
      >
        Gửi đặt lịch
      </button>
    </form>

    <div
      v-if="successMessage"
      class="mt-4 text-green-600 text-center font-semibold"
    >
      {{ successMessage }}
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  name: "",
  phone: "",
  date: "",
  time: "",
  note: "",
});

const successMessage = ref("");

const submitBooking = () => {
  // Giả lập gửi dữ liệu
  console.log("Dữ liệu đặt lịch:", form.value);

  successMessage.value = "Đặt lịch thành công! Chúng tôi sẽ liên hệ sớm.";
  form.value = {
    name: "",
    phone: "",
    date: "",
    time: "",
    note: "",
  };
};
</script>
