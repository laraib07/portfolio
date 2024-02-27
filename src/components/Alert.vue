<script setup>
defineProps({
  alert: {
    type: Object,
    required: true,
  },
});
</script>
<template>
  <span
    :class="{
      'text-error-content bg-error': !alert.success,
      'text-success-content bg-success': alert.success,
    }"
    class="fixed left-0 right-0 top-16 text-center p-4 z-50"
    v-show="alert.message"
    >{{ alert.message }}</span
  >
</template>
