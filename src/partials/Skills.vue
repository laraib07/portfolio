<script setup>
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
      <h1 class="text-4xl font-semibold sm:text-6xl">Skills</h1>

      <template v-for="skill of skills" :key="skill.title">
        <div class="pt-6">
          <h2 class="text-2xl font-medium" v-text="skill.title"></h2>
          <div class="flex flex-wrap gap-2 pt-3">
            <span
              v-for="name of skill.skills"
              class="btn btn-outline btn-sm border-2"
              v-text="name"
            ></span>
          </div>
        </div>
      </template>
    </div>
  </section>
</template>
