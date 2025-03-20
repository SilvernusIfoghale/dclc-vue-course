<script setup>
import jobData from "@/jobs2.json";
import JobListing from "./JobListing.vue";
import { ref } from "vue";

const jobs = ref(jobData);
// console.log(jobs.value);
</script>

<template>
  <div class="flex justify-center mx-5">
    <div class="">
      <p>job listings</p>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <JobListing v-for="job in jobs" :key="job.id" :job="job" />
      </div>
    </div>
  </div>
</template>
