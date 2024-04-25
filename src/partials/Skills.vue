<script setup>
import SkillItem from "@/components/SkillItem.vue";
defineProps({
  skills: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section id="skills" class="w-full px-4 py-16 bg-base-300">
    <div class="mx-auto max-w-screen-lg">
      <h2
        class="text-4xl font-semibold tracking-tight leading-tight sm:text-6xl"
      >
        Skills
      </h2>

      <template v-for="skill of skills" :key="skill.title">
        <div class="mt-4">
          <h3 class="text-base font-medium" v-text="skill.title"></h3>
          <div class="flex flex-wrap gap-1 mt-2 text-xs">
            <SkillItem v-for="name of skill.skills" v-text="name"></SkillItem>
          </div>
        </div>
      </template>
    </div>
  </section>
</template>
