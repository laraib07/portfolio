<script setup>
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
      <div class="flex flex-wrap gap-2 text-sm">
        <SkillItem v-for="skill of project.skills" :skill="skill" />
      </div>
      <h2 class="font-medium text-2xl py-2" v-text="project.title"></h2>
      <p class="text-sm" v-text="project.desc"></p>
    </div>
    <div class="flex flex-row w-full p-4 gap-2">
      <a
        :href="project.gitlink"
        target="_blank"
        v-show="project.gitlink"
        class="btn btn-outline border-2 w-1/2 grow"
      >
        Github
      </a>
      <a
        :href="project.demo"
        target="_blank"
        v-show="project.demo"
        class="btn btn-neutral w-1/2 grow"
      >
        Visit
      </a>
    </div>
  </div>
</template>
