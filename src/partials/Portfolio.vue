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
    <div class="mx-auto max-w-screen-xl lg:w-4/5">
      <h1 class="text-4xl font-semibold sm:text-6xl">Portfolio</h1>
      <div class="grid grid-cols-1 gap-8 pt-6 sm:grid-cols-2 lg:grid-cols-3">
        <ProjectItem v-for="project of projects" :project="project" />

        <div class="flex items-center justify-center">
          <a
            href="https://github.com/laraib07"
            target="_blank"
            class="btn btn-outline border-2 group"
          >
            See more
            <span class="inline-block duration-200 group-hover:translate-x-2"
              >&nbsp;&#10230;
            </span>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
