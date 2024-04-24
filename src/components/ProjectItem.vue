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
    class="flex flex-col rounded-md overflow-hidden group bg-base-100 shadow-sm duration-500 ease-in-out hover:shadow-lg"
  >
    <div class="relative h-[150px] overflow-hidden flex justify-center">
      <img
        :src="project.imgsrc"
        :alt="project.title"
        class="object-cover w-full blur-sm"
      />
      <img
        :src="project.imgsrc"
        :alt="project.title"
        class="absolute object-contain h-full ease-in-out duration-500 group-hover:scale-110"
      />
    </div>
    <div class="p-4 grow">
      <div class="flex flex-wrap gap-2 text-sm">
        <SkillItem v-for="skill of project.skills" :skill="skill" />
      </div>
      <h3 class="font-medium text-2xl py-2" v-text="project.title"></h3>
      <p class="text-sm" v-text="project.desc"></p>
    </div>
    <div class="flex p-4 gap-2">
      <a
        :href="project.gitlink"
        target="_blank"
        v-if="project.gitlink"
        class="btn btn-outline border-2 flex-1"
      >
        Github
      </a>
      <a
        :href="project.demo"
        target="_blank"
        v-if="project.demo"
        class="btn btn-neutral flex-1"
      >
        Visit
      </a>
    </div>
  </div>
</template>
