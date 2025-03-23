<script setup>
import { defineProps } from "vue";
import { RouterLink } from "vue-router";
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
  link: {
    type: String,
  },
});
</script>

<template>
  <div :class="`${bg} p-5 rounded-xl w-80`">
    <h1 class="font-bold text-xl">{{ title }}</h1>
    <p class="text-sm py-2">{{ subtitle }}</p>
    <RouterLink :to="`${link}`" :class="`${btnBg} text-white rounded-lg py-1 px-3 text-xs`">{{
      btnTitle
    }}</RouterLink>
  </div>
</template>
