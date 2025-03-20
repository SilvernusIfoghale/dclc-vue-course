<script setup>
import { defineProps } from "vue";

defineProps({
  job: Object,
});
</script>

<template>
  <div class="rounded-xl w-80 bg-green-50 p-5 font-semibold text-sm">
    <h1>{{ job.type }}</h1>
    <h2 class="font-bold text-lg">{{ job.title }}</h2>

    <p class="text-xs py-3">
      {{ job.description }}
    </p>
    <p class="py-2 text-green-600">{{ job.salary }}</p>
    <p class="py-1 text-red-900 text-xs">{{ job.location }}</p>
    <button class="bg-green-500 w-full rounded-sm py-1.5 mt-1 text-white text-xs">Read More</button>
  </div>
</template>
