<!-- components/MenuItem.vue -->
<template>
  <div
    class="bg-white p-4 rounded-lg shadow-lg border-l-4 border-yellow-500 hover:bg-yellow-100 transition duration-200"
  >
    <h2 class="text-xl font-bold text-red-600">{{ item.name }}</h2>
    <p class="text-gray-700">{{ item.description }}</p>
    <p class="text-yellow-600 font-bold mt-2">${{ item.price }}</p>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  item: {
    type: Object,
    required: true,
  },
});
</script>
