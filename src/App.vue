<script setup>
import Card from "./components/Card.vue";
import q from "./data/quizes.json";
import { ref, watch } from "vue";

const quizes = ref(q);
const search = ref("");

watch(search, () => {
  quizes.value = q.filter((quiz) =>
    quiz.name.toLowerCase().includes(search.value.toLowerCase())
  );
});
</script>

<template>
  <div class="mx-auto max-w-[1000px]">
    <header class="pt-20 flex flex-row items-center gap-20">
      <h1 class="text-4xl font-bold cursor-pointer">Quizes</h1>
      <input
        v-model.trim()="search"
        type="text"
        placeholder="Search..."
        class="border border-black py-2 px-5 bg-slate-100 placeholder:text-black rounded-md focus:outline-none focus:scale-105 transition-all duration-300"
      />
    </header>
    <!-- Cards -->
    <div class="flex flex-row gap-20">
      <!-- Card -->
      <Card v-for="quiz in quizes" :key="quiz.id" :quiz="quiz" />
    </div>
  </div>
</template>
