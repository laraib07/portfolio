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
    <div class="grid gap-4 mx-auto max-w-screen-lg lg:grid-cols-5 lg:gap-6">
      <h2
        class="text-4xl font-semibold tracking-tight leading-tight sm:text-6xl lg:col-span-2"
      >
        Experience
      </h2>
      <div class="lg:col-span-3">
        <ExperienceItem v-for="exp of experience" :experience="exp" />
      </div>
    </div>
  </section>
</template>
