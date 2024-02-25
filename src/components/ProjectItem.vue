<script setup>
import Github from "../components/icons/Github.vue";
import SkillItem from "./SkillItem.vue";

defineProps({
  project: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div
    class="flex flex-col w-full rounded-md overflow-hidden group bg-base-100 shadow-sm duration-500 ease-in-out hover:shadow-lg"
  >
    <div class="w-full h-[150px] overflow-hidden">
      <img
        :src="project.imgsrc"
        :alt="project.title"
        class="object-fit ease-in-out duration-500 group-hover:scale-110"
      />
    </div>
    <div class="p-4 grow">
      <div class="flex flex-wrap gap-2 text-xs">
        <SkillItem v-for="skill of project.skills" :skill="skill" />
      </div>
      <h2 class="font-medium text-2xl py-2" v-text="project.title"></h2>
      <p class="text-sm" v-text="project.desc"></p>
    </div>
    <div class="items-start bg-base-300 w-full px-4 py-8">
      <div class="relative flex items-center bg-base-300 w-full">
        <a
          :href="project.gitlink"
          target="_blank"
          v-show="project.gitlink"
          class="absolute left-0 hover:opacity-85"
        >
          <Github />
        </a>
        <a
          :href="project.demo"
          target="_blank"
          v-show="project.demo"
          class="btn btn-outline btn-sm absolute right-0"
        >
          Demo
        </a>
      </div>
    </div>
  </div>
</template>
