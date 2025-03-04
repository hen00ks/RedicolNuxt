<template>
  <div class="relative w-fit">
    <div
      class="size-80 bg-primary-light/50 backdrop-blur-md rounded-full overflow-clip"
    >
      <img :src="props.imageUrl" alt="" class="object-cover size-full" />
    </div>
    <div
      class="absolute -bottom-10 -right-10 -z-10 size-36 blur-xs bg-primary-dark rounded-full"
    />
    <div
      class="absolute -top-10 -left-10 size-36 bg-primary-light rounded-full"
    />
  </div>
</template>
<script setup lang="ts">
const props = defineProps<{ imageUrl?: string }>();
</script>
