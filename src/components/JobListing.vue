<script setup>
import { defineProps, ref, computed } from "vue";
import { RouterLink } from "vue-router";

const props = defineProps({
  job: Object,
});

const showFullDescription = ref(false);

const truncatedDescription = computed(() => {
  let description = props.job.description;
  if (!showFullDescription.value) {
    description = description.substring(0, 130) + "...";
  }
  return description;
});

const toggleFullDescription = () => {
  showFullDescription.value = !showFullDescription.value;
};
</script>

<template>
  <div class="rounded-xl w-80 bg-green-50 p-5 font-semibold text-sm shadow-sm">
    <h1>{{ job.type }}</h1>
    <h2 class="font-bold text-lg">{{ job.title }}</h2>

    <div class="text-xs py-3">
      <p>{{ truncatedDescription }}</p>
      <button
        @click="toggleFullDescription"
        class="mt-2 text-green-500 hover:text-green-600 cursor-pointer"
      >
        {{ showFullDescription ? "Less" : "More" }}
      </button>
    </div>
    <p class="py-2 text-green-600 text-xs">{{ job.salary }} / Year</p>
    <div class="flex justify-between items-center border-t-[1.5px] border-gray-200 py-2">
      <p class="py-1 text-red-900 text-xs">
        <i class="pi pi-map-marker text-orange-700"></i> {{ job.location }}
      </p>
      <RouterLink
        :to="'/jobs/' + job.id"
        class="bg-green-500 w-20 block text-center rounded-sm py-1.5 mt-1 text-white text-xs hover:bg-green-400"
        >Read More</RouterLink
      >
    </div>
  </div>
</template>
