<script setup>
import SkillItem from "./SkillItem.vue";

defineProps({
  experience: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="text-base text-base-content mt-8 first-of-type:mt-0">
    <h3 class="font-semibold">
      {{ experience.designation }} | {{ experience.company }}
    </h3>
    <time class="mt-1 block text-base-content/80">
      {{ experience.from }} - {{ experience.to }}
    </time>
    <p class="mt-2 text-base">
      {{ experience.description }}
    </p>
    <div class="flex flex-wrap gap-1 mt-2 text-xs">
      <SkillItem v-for="skill of experience.skills" :skill="skill" />
    </div>
  </div>
</template>
