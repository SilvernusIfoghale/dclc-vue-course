<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <section>
    <div class="m-auto py-6 px-6">
      <RouterLink to="jobs.html" class="text-green-500 hover:text-green-600 flex items-center">
        <i class="pi pi-arrow-circle-left mr-2"> Back to Job Listings</i>
      </RouterLink>
    </div>
  </section>
</template>
