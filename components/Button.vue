<template>
    <button class="tw-w-40 tw-h-12 tw-bg-blue-500 tw-text-white tw-rounded-lg tw-shadow-md hover:tw-bg-blue-600 tw-flex tw-items-center tw-justify-center">
      {{ $props.label }}
    </button>
</template>
<script setup lang="ts">  
const props = defineProps({
  label: {
    type: String,
    default: ""
  }
})
</script>