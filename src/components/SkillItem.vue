<script setup>
defineProps({
  skill: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <span
    class="border border-base-content/50 text-base-content/80 rounded-full py-1 px-2"
    v-text="skill"
  ></span>
</template>
