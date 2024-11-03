<template>
  <!-- Main page -->
  <div class="w-screen h-screen py-15 p-x10 flex justify-center items-center">
    <!-- Yellow box -->
    <div
      class="w-[80%] h-[80%] border-8 border-[#ffb80e] flex flex-row relative bg-[#982121] rounded-3xl"
    >
      <!-- Logo -->
      <div class="absolute top-6 left-12 flex flex-row gap-3 items-center">
        <img src="../UI/logo.png" alt="Pir BaBa's logo" class="w-20 h-20" />
        <p class="font-bold text-5xl text-white">Pir BaBa</p>
      </div>

      <!-- Hamburger PIC -->
      <div class="w-[40%] flex justify-center items-center">
        <img src="../UI/pic1.png" alt="Hamburger PIC" class="w-[90%] mt-32" />
      </div>

      <!-- Login -->
      <div class="w-[60%] flex justify-center items-center">
        <div class="flex flex-col gap-4 w-[80%]">
          <h2 class="text-3xl font-semibold text-white mb-10">
            <span class="text-6xl">Welcome,</span><br />please fill out your
            info
          </h2>

          <!-- Customer INFO -->
          <div class="flex flex-col gap-2">
            <!-- Customer name -->
            <label for="customerName" class="text-white text-lg">name: </label>
            <input
              type="text"
              name="cutomerName"
              id="customrName"
              class="w-[60%] h-8 p-5 rounded-lg"
              placeholder="james maccafie"
            />

            <!-- Customer table -->
            <label for="customerName" class="text-white text-lg mt-4"
              >Table:
            </label>
            <input
              type="number"
              name="cutomerName"
              id="customrName"
              class="w-[60%] h-8 rounded-lg p-5"
              placeholder="6"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped></style>
