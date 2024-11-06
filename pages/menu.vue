<!-- pages/menu.vue -->
<template>
  <div class="container mx-auto p-4 bg-yellow-50 min-h-screen">
    <!-- نوار خوش‌آمدگویی -->
    <div
      class="bg-red-500 text-white text-lg font-semibold p-3 rounded-lg mb-4 shadow-lg"
    >
      Welcome, {{ customerName }}! Your table number is {{ tableNumber }}.
    </div>

    <!-- عنوان منو -->
    <h1 class="text-3xl font-extrabold text-red-600 mb-6 text-center">Menu</h1>

    <!-- محتوای منو اینجا قرار می‌گیرد -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <!-- نمونه کارت منو -->
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
      <!-- تکرار کارت منو برای آیتم‌های دیگر -->
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
      <div
        class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200 cursor-pointer"
      >
        <h2 class="text-xl font-bold text-red-600">Burger</h2>
        <p class="text-gray-700">
          Juicy and delicious burger with special sauce.
        </p>
        <p class="text-yellow-600 font-bold mt-2">$5.99</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
const customerName = route.query.name || "Guest";
const tableNumber = route.query.table || "Unknown";
</script>

<style scoped>
.container {
  background-color: #fef9c3; /* رنگ زمینه زرد کم‌رنگ */
}

.bg-red-500 {
  background-color: #ef4444;
}

.text-red-600 {
  color: #dc2626;
}

.border-yellow-500 {
  border-color: #fbbf24;
}

.bg-yellow-50 {
  background-color: #fffbeb;
}
</style>
