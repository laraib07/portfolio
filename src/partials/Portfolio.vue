<script setup>
import ProjectItem from "../components/ProjectItem.vue";

defineProps({
  projects: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section id="portfolio" class="w-full px-4 py-16 bg-base-200">
    <div class="mx-auto max-w-screen-lg">
      <h2 class="text-4xl font-semibold sm:text-6xl">Portfolio</h2>
      <div class="grid gap-8 mt-4 sm:grid-cols-2 lg:grid-cols-3">
        <ProjectItem v-for="project of projects" :project="project" />

        <a
          href="https://github.com/laraib07"
          target="_blank"
          class="grid place-items-center"
        >
          <p class="group text-blue-500 hover:underline">
            See more
            <span class="inline-block duration-200 group-hover:translate-x-2"
              >&nbsp;&#10230;
            </span>
          </p>
        </a>
      </div>
    </div>
  </section>
</template>
