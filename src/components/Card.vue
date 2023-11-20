<script setup>
import { defineProps } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();

const { quiz } = defineProps(["quiz"]);

const navigateToQuiz = () => {
  router.push(`/quiz/${quiz.id}`);
};
</script>

<template>
  <div
    @click="navigateToQuiz"
    class="flex flex-col rounded-xl bg-gray-300 w-[300px] mt-16 transition-all duration-500 hover:scale-105 cursor-pointer"
  >
    <img
      :src="quiz.img"
      alt="frontEndImage"
      class="w-[300px] h-[250px] rounded-t-xl"
    />
    <div class="flex flex-col gap-5 p-5">
      <h1 class="text-lg font-bold">{{ quiz.name }}</h1>
      <p class="font-bold text-gray-500">
        {{ quiz.questions.length }} questions
      </p>
    </div>
  </div>
</template>
