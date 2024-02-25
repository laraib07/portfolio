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
    class="border border-base-content rounded-full py-1 px-2"
    v-text="skill"
  ></span>
</template>
