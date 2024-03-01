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
  <div class="pt-8 first-of-type:pt-0">
    <h4 class="font-semibold text-base-content">
      {{ experience.designation }} | {{ experience.company }}
    </h4>
    <time class="pt-2 block text-sm text-base-content">
      {{ experience.from }} - {{ experience.to }}
    </time>
    <p class="pt-2 text-sm text-base-content">
      {{ experience.description }}
    </p>
    <div class="flex flex-wrap gap-2 pt-4 text-sm">
      <SkillItem v-for="skill of experience.skills" :skill="skill" />
    </div>
  </div>
</template>
