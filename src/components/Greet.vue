<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <p>Hi, I am {{ name }}</p>
</template>

<style scoped>
p {
  -webkit-text-stroke: 2.5px;
  -webkit-text-fill-color: var(
    --fallback-b1,
    oklch(var(--b1) / var(--tw-bg-opacity))
  );
}
</style>
