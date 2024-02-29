<script setup>
import ExperienceItem from "@/components/ExperienceItem.vue";

defineProps({
  experience: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section id="experience" class="w-full px-4 py-16 bg-base-300">
    <div class="flex flex-col mx-auto max-w-screen-xl lg:flex-row lg:w-[90vw]">
      <h1 class="inline text-4xl font-semibold sm:text-6xl pr-8">Experience</h1>
      <div class="flex flex-col pt-6 lg:pl-8 lg:w-3/4 lg:pt-0">
        <ExperienceItem v-for="exp of experience" :experience="exp" />
      </div>
    </div>
  </section>
</template>
