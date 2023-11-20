<script setup></script>

<template>
  <div class="mx-auto max-w-[1000px]">
    <header class="pt-20 flex flex-row items-center gap-20">
      <h1 class="text-4xl font-bold">Quizes</h1>
      <input
        type="text"
        placeholder="Search..."
        class="border border-black py-2 px-5 bg-slate-100 placeholder:text-black rounded-md focus:outline-none focus:scale-105 transition-all duration-300"
      />
    </header>
    <!-- Card -->
    <div
      class="flex flex-col rounded-xl bg-gray-300 w-[300px] mt-16 transition-all duration-500 hover:scale-105 cursor-pointer"
    >
      <img
        src="/src/assets/front.png"
        alt="frontEndImage"
        class="w-[300px] h-[250px] rounded-t-xl"
      />
      <div class="flex flex-col gap-5 p-5">
        <h1 class="text-lg font-bold">Front-end Development</h1>
        <p class="font-bold text-gray-500">15 Questions</p>
      </div>
    </div>
  </div>
</template>
