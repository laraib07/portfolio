<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <p class="bg-base-100 bg-clip-text">Hi, I am {{ name }}</p>
</template>

<style scoped>
p {
  -webkit-text-stroke: 2.5px
    var(--fallback-bc, oklch(var(--bc) / var(--tw-bg-opacity)));
  -webkit-text-fill-color: var(
    --fallback-b1,
    oklch(var(--b1) / var(--tw-bg-opacity))
  );
}
</style>
