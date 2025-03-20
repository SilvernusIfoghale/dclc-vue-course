<script setup>
import { defineProps } from "vue";
defineProps({
  title: {
    type: String,
    default: "Become a Vue Dev",
  },
  subtitle: {
    type: String,
    default: "Find vue job that fits your skills and needs",
  },
});
</script>

<template>
  <div
    class="flex justify-center flex-col items-center py-16 text-white bg-emerald-600 border-t-[1.5px] border-emerald-500"
  >
    <h1 class="text-2xl font-bold leading-10">{{ title }}</h1>
    <p>{{ subtitle }}</p>
  </div>
</template>
