<script setup>
import Question from "../components/Question.vue";
import QuizHeader from "../components/QuizHeader.vue";
import { useRoute } from "vue-router";
import { ref, watch, computed } from "vue";
import quizes from "../data/quizes.json";

const route = useRoute();
const quizId = parseInt(route.params.id);
const quiz = quizes.find((q) => q.id === quizId);
const currentQuestionIndex = ref(0);

const questionStatus = computed(() => {
  return `${currentQuestionIndex.value} / ${quiz.questions.length}`;
});
</script>

<template>
  <div>
    <QuizHeader :questionStatus="questionStatus" />
    <Question :question="quiz.questions[currentQuestionIndex]" />
    <button @click="currentQuestionIndex++">Next Question</button>
  </div>
</template>
