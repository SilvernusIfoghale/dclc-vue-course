<script setup>
import HeroSection from "@/components/HeroSection.vue";
import HomeCards from "@/components/HomeCards.vue";
import JobListings from "@/components/jobListings.vue";
</script>

<template>
  <HeroSection title="Become a Vue Dev" subtitle="Find vue job that fits your skills and needs" />
  <HomeCards />
  <JobListings :limit="3" :show-button="true" />
</template>
