<template>
  <div class="relative w-fit">
    <div
      class="w-[min(320px,70dvw)] aspect-square bg-primary-light/50 backdrop-blur-md rounded-full overflow-clip"
    >
      <img :src="props.imageUrl" alt="" class="object-cover size-full" />
    </div>
    <div
      class="absolute -bottom-10 -right-10 -z-10 size-36 blur-xs bg-primary-dark rounded-full"
    />
    <div
      class="top absolute -top-10 -left-10 size-32 bg-primary-light rounded-full"
      :class="bgColor"
    />
  </div>
</template>
<script setup lang="ts">
const props = defineProps<{ imageUrl?: string; bgColor?: string }>();
</script>
<style scoped>
.top {
  animation: top-anim 1s ease-out;
  animation-timeline: view();
  animation-range-end: contain;
  animation-range-start: entry;
}
/* .bottom {
  scale: 2;
  transform-origin: bottom right;
  animation: bottom-anim 1s ease-out forwards;
  animation-timeline: view();
  animation-range-end: contain;
  animation-range-start: entry;
} */
@keyframes top-anim {
  from {
    scale: 0.5;
  }
}
/* @keyframes bottom-anim {
  to {
    scale: 1;
  }
} */
</style>
