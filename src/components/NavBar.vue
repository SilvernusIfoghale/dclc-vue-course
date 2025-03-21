<script setup>
import logo from "@/assets/logo.svg";
</script>

<template>
  <nav
    class="flex justify-center gap-5 sm:justify-between items-center px-5 h-16 bg-emerald-600 text-white"
  >
    <div class="w-9 h-9 bg-white flex justify-center items-center rounded-full">
      <img :src="logo" alt="vue logo" class="w-5 h-6" />
    </div>
    <ul class="flex gap-3">
      <li>
        <a href="/" class="hover:bg-green-900 p-1.5 duration-500 bg-green-900 rounded-sm">Home</a>
      </li>
      <li><a href="/jobs" class="hover:bg-green-900 p-1.5 duration-500 rounded-sm">Jobs</a></li>
      <li>
        <a href="/jobs/add" class="hover:bg-green-900 p-1.5 duration-500 rounded-sm">Add Job</a>
      </li>
    </ul>
  </nav>
</template>
