<script setup>
import { defineProps } from "vue";

const { question } = defineProps(["question"]);
</script>

<template>
  <div class="mt-5">
    <!-- Question -->
    <div class="text-3xl">
      <h1>{{ question.text }}</h1>
    </div>
    <!-- Options -->
    <div
      v-for="option in question.options"
      :key="option.id"
      class="mt-5 bg-orange-100 cursor-pointer"
    >
      <div class="flex items-center gap-5">
        <p
          class="w-12 h-12 items-center bg-orange-400 text-center flex justify-center font-bold text-lg"
        >
          {{ option.label }}
        </p>
        <div>
          <p>{{ option.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
