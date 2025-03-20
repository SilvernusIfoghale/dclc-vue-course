<script setup>
import SingleCard from "./SingleCard.vue";
</script>

<template>
  <div
    class="flex flex-col sm:flex-row justify-center items-center my-10 mx-5 gap-5 font-semibold text-sm"
  >
    <SingleCard
      bg="bg-gray-100"
      title="For Developers"
      subtitle="Browse our Vue jobs and start your career today"
      btnTitle="Browse Jobs"
      btnBg="bg-blue-950"
    />
    <SingleCard
      bg="bg-green-100"
      title="For Employers"
      subtitle="List your job to find the perfect developer for the role"
      btnTitle="Add Job"
      btnBg="bg-green-500"
    />
  </div>
</template>
