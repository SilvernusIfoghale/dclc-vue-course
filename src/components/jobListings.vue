<script setup>
import jobData from "@/jobs2.json";
import JobListing from "./JobListing.vue";
import { ref, defineProps } from "vue";

const jobs = ref(jobData);
defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false,
  },
});
// console.log(jobs.value);
</script>

<template>
  <div class="flex justify-center mx-5">
    <div class="">
      <p class="text-green-500 text-xl font-bold text-center py-5">Browse Jobs</p>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <JobListing v-for="job in jobs.slice(0, limit || jobs.length)" :key="job.id" :job="job" />
      </div>
    </div>
  </div>
  <div v-if="showButton" class="text-center my-10">
    <a class="bg-black py-2 px-16 rounded-lg text-white text-xs hover:bg-gray-700" href="/jobs"
      >View All Jobs</a
    >
  </div>
</template>
