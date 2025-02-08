<script setup lang="ts">
import { computed } from 'vue';

const props = withDefaults(
  defineProps<{
    size?: 'A4';
  }>(),

  {
    size: 'A4',
  }
);

const pageSize = computed(() => {
  switch (props.size) {
    case 'A4':
      return 'w-[210mm] h-[297mm]';
    default:
      return 'w-[210mm] h-[297mm]';
  }
});
</script>

<template>
  <div :class="[pageSize, 'bg-white shadow']">
    <slot />
  </div>
</template>
