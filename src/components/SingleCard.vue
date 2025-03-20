<script setup>
import { defineProps } from "vue";
defineProps({
  title: {
    type: String,
    default: "Loading,...",
  },
  subtitle: {
    type: String,
    default: "Loading,...",
  },
  btnTitle: {
    type: String,
    default: "Loading,...",
  },
  bg: {
    type: String,
    default: "bg-white",
  },
  btnBg: {
    type: String,
    default: "bg-blue-950",
  },
});
</script>

<template>
  <div :class="`${bg} p-5 rounded-xl w-80`">
    <h1 class="font-bold text-xl">{{ title }}</h1>
    <p class="text-sm py-2">{{ subtitle }}</p>
    <button :class="`${btnBg} text-white rounded-lg py-1 px-3 text-xs`">{{ btnTitle }}</button>
  </div>
</template>
