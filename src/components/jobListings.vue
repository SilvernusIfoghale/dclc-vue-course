<script setup>
import axios from "axios";
import JobListing from "./JobListing.vue";
import { defineProps, onMounted, reactive } from "vue";
import { RouterLink } from "vue-router";
import PulseLoader from "vue-spinner/src/PulseLoader.vue";

const state = reactive({
  jobs: [],
  isLoading: true,
});
defineProps({
  limit: Number,
  showButton: {
    type: Boolean,
    default: false,
  },
});

onMounted(async () => {
  try {
    const response = await axios.get("/api/jobs");
    state.jobs = response.data;
  } catch (error) {
    console.log("Error", error);
  } finally {
    state.isLoading = false;
  }
});
// console.log(jobs.value);
</script>

<template>
  <div class="bg-blue-50 py-10">
    <div class="flex justify-center mx-5 py-10">
      <div class="">
        <p class="text-green-500 text-xl font-bold text-center py-5">Browse Jobs</p>
        <div v-if="state.isLoading" class="text-center text-gray-500 py-6">
          <PulseLoader />
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <JobListing
            v-for="job in state.jobs.slice(0, limit || state.jobs.length)"
            :key="job.id"
            :job="job"
          />
        </div>
      </div>
    </div>
    <div v-if="showButton" class="text-center my-10">
      <RouterLink
        class="bg-black py-2 px-16 rounded-lg text-white text-xs hover:bg-gray-700"
        to="/jobs"
        >View All Jobs</RouterLink
      >
    </div>
  </div>
</template>
