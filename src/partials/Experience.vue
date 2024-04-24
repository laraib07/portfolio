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
    <div class="flex flex-col mx-auto max-w-screen-lg lg:flex-row">
      <h1 class="inline text-4xl font-semibold sm:text-6xl">Experience</h1>
      <div class="pt-6 lg:pt-0 lg:pl-16 lg:w-3/4">
        <ExperienceItem v-for="exp of experience" :experience="exp" />
      </div>
    </div>
  </section>
</template>
