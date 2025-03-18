<script setup>
const props = defineProps({
  header: String,
});
</script>
<template>
  <div class="space-y-4 max-w-7xl place-self-center place-items-center">
    <h2 class="header">{{ header }}</h2>
    <div
      class="parent w-full grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4 overflow-x-auto md:overflow-visible"
    >
      <!-- Row 1 -->
      <div class="aspect-square">
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div
        class="md:col-span-2 relative group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">Name reveal</p>
        </div>
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div class="aspect-square">
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div class="md:col-span-2 relative group">
        <div class="absolute size-full bg-amber-300"></div>
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>

      <!-- Row 2 -->
      <div class="md:col-span-2 relative group">
        <div class="absolute size-full bg-amber-300"></div>
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div class="aspect-square">
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div class="md:col-span-2 relative group">
        <div class="absolute size-full bg-amber-300"></div>
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
      <div class="aspect-square">
        <img
          src="/images/coffee-beans.png"
          alt="images"
          class="size-full object-cover"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.parent > div {
  border-radius: var(--radius-xl);
  overflow: clip;
  max-height: calc(48px * 4);
}
</style>
