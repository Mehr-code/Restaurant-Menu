<template>
  <!-- Main page -->
  <div class="w-screen h-screen flex justify-center items-center bg-white p-4">
    <!-- Yellow box -->
    <div
      class="w-full max-w-5xl h-full md:h-[90%] border-8 border-[#ffb80e] flex flex-col md:flex-row relative bg-[#982121] rounded-3xl"
    >
      <!-- Logo -->
      <div class="absolute top-4 left-6 flex flex-row gap-3 items-center">
        <img
          src="../UI/logo.png"
          alt="Pir BaBa's logo"
          class="w-16 h-16 md:w-20 md:h-20"
        />
        <p class="font-bold text-3xl md:text-5xl text-white">Pir BaBa</p>
      </div>

      <!-- Hamburger PIC -->
      <div
        class="w-full md:w-[40%] flex justify-center items-center p-4 md:p-0"
      >
        <img
          src="../UI/pic1.png"
          alt="Hamburger PIC"
          class="w-3/4 md:w-[90%] mt-12 md:mt-32"
        />
      </div>

      <!-- Login -->
      <div class="w-full md:w-[60%] flex justify-center items-center p-4">
        <form
          class="flex flex-col gap-4 w-full max-w-sm"
          @submit.prevent="goToMenu"
        >
          <h2 class="text-3xl md:text-4xl font-semibold text-white mb-3">
            Welcome :))
          </h2>
          <h3 class="text-xl md:text-2xl text-white mb-5">
            Please fill out your info
          </h3>

          <!-- Customer INFO -->

          <!-- Customer name -->
          <label for="customerName" class="text-white text-lg">Name:</label>
          <input
            required
            v-model="name"
            type="text"
            id="customerName"
            class="w-full h-12 p-3 rounded-lg"
            placeholder="e.g., James McCaffrey..."
          />

          <!-- Customer table -->
          <label for="tableNumber" class="text-white text-lg">Table:</label>
          <input
            required
            v-model="tableNumber"
            type="number"
            id="tableNumber"
            class="w-full h-12 p-3 rounded-lg mb-5"
            placeholder="e.g., 6"
          />

          <!-- Login button -->
          <button
            type="submit"
            class="text-lg text-yellow-400 hover:text-white border-4 border-yellow-400 hover:bg-yellow-500 focus:ring-4 focus:outline-none focus:ring-yellow-300 font-medium rounded-lg px-5 py-2.5 text-center mb-2 dark:border-yellow-300 dark:text-yellow-300 dark:hover:text-white dark:hover:bg-yellow-400 dark:focus:ring-yellow-900 w-full"
          >
            Login
          </button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { useRouter } from "vue-router";
import { ref } from "vue";

const router = useRouter();
const name = ref("");
const tableNumber = ref("");

const goToMenu = () => {
  router.push({
    path: "/menu",
    query: { name: name.value, table: tableNumber.value },
  });
};
</script>

<style scoped></style>
