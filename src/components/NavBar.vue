<script setup>
import logo from "@/assets/logo.svg";
import { RouterLink, useRoute } from "vue-router";

const isActiveLink = (routePath) => {
  const route = useRoute();
  return route.path === routePath;
};
</script>

<template>
  <nav
    class="flex justify-center gap-5 sm:justify-between items-center px-5 h-16 bg-emerald-600 text-white"
  >
    <RouterLink to="/" class="flex gap-2 items-center">
      <div class="w-9 h-9 bg-white flex justify-center items-center rounded-full">
        <img :src="logo" alt="vue logo" class="w-5 h-6" />
      </div>
      <h1 class="font-bold text-lg">Vue Jobs</h1>
    </RouterLink>
    <ul class="flex gap-3">
      <li>
        <RouterLink
          to="/"
          :class="[
            isActiveLink('/') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white',
            'text-white',
            'px-3',
            'py-1',
            'rounded-md',
          ]"
          >Home</RouterLink
        >
      </li>
      <li>
        <RouterLink
          to="/jobs"
          :class="[
            isActiveLink('/jobs') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white',
            'text-white',
            'px-3',
            'py-1',
            'rounded-md',
          ]"
          >Jobs</RouterLink
        >
      </li>
      <li>
        <RouterLink
          to="/jobs/add"
          :class="[
            isActiveLink('/jobs/add') ? 'bg-green-900' : 'hover:bg-gray-900 hover:text-white',
            'text-white',
            'px-3',
            'py-1',
            'rounded-md',
          ]"
          >Add Job</RouterLink
        >
      </li>
    </ul>
  </nav>
</template>
