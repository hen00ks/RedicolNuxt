<template>
  <div class="relative w-fit">
    <div
      class="size-80 bg-primary-light/50 backdrop-blur-md rounded-full overflow-clip"
    >
      <img :src="props.imageUrl" alt="" class="object-cover size-full" />
    </div>
    <div
      class="bottom absolute -bottom-10 -right-10 -z-10 size-36 blur-xs bg-primary-dark rounded-full"
    />
    <div
      class="top absolute -top-10 -left-10 size-36 bg-primary-light rounded-full"
    />
  </div>
</template>
<script setup lang="ts">
const props = defineProps<{ imageUrl?: string }>();
</script>
<style scoped>
.top {
  animation: top-anim 1s ease-out;
  animation-timeline: view();
  animation-range-end: contain;
  animation-range-start: entry;
}
.bottom {
  transform-origin: bottom right;
  animation: bottom-anim 1s ease-out;
  animation-timeline: view();
  animation-range-end: contain;
  animation-range-start: entry;
}
@keyframes top-anim {
  from {
    scale: 0.7;
  }
}
@keyframes bottom-anim {
  from {
    scale: 2;
  }
  to {
    scale: 1;
  }
}
</style>
