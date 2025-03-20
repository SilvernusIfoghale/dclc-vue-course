<script setup lang="ts">
import HeroSection from "./components/HeroSection.vue";
import HomeCards from "./components/HomeCards.vue";
import JobListings from "./components/jobListings.vue";
import NavBar from "./components/NavBar.vue";
</script>

<template>
  <NavBar />
  <HeroSection title="Become a Vue Dev" subtitle="Find vue job that fits your skills and needs" />
  <HomeCards />
  <JobListings />
</template>
