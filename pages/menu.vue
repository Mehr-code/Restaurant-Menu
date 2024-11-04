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
      <!-- کارت‌های منو -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
        <MenuItem
          v-for="(item, index) in menuItems"
          :key="index"
          :item="item"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { useRoute } from "vue-router";
import MenuItem from "~/component/MenuItem.vue";
// import axios from "axios";

const route = useRoute();
const customerName = route.query.name || "Guest";
const tableNumber = route.query.table || "Unknown";
const menuItem = ref([]);

// فراخوانی API برای دریافت داده‌ها
const fetchMenuItems = async () => {
  try {
    const response = await useFetch("https://api.example.com/menu");
    menuItems.value = response.data;
  } catch (error) {
    console.error("Error fetching menu items:", error);
  }
};

// دریافت داده‌ها هنگام بارگذاری صفحه
onMounted(() => {
  fetchMenuItems();
});
</script>

<style scoped>
.container {
  background-color: #fef9c3; /* رنگ زمینه زرد کم‌رنگ */
}

.bg-red-500 {
  background-color: #e32929;
}

.text-red-600 {
  color: #dc2626;
}

.border-yellow-500 {
  border-color: #ffb80e;
}

.bg-yellow-50 {
  background-color: #fffbeb;
}
</style>
