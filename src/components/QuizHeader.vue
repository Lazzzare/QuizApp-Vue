<script setup>
import { defineProps } from "vue";

const { questionStatus } = defineProps(["questionStatus"]);
</script>

<template>
  <header class="mt-10 text-3xl">
    <h4>Question {{ questionStatus }}</h4>
    <div class="bar">
      <div class="completion"></div>
    </div>
  </header>
</template>

<style scoped>
.bar {
  width: 300px;
  height: 50px;
  border: 3px solid bisque;
}

.completion {
  height: 100%;
  width: 0%;
  background-color: bisque;
}
</style>
