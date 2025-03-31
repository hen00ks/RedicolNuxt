<template>
  <div class="mb-12 bg-linear-to-r via-primary-light/50 w-full p-4">
    <ul class="flex sm:gap-8 sm:justify-center justify-between">
      <li
        :class="currentTab === 'fruits' && 'border-b-3 border-b-primary'"
        class="cursor-pointer w-24 text-center"
        @click="$emit('changeTab', 'fruits')"
      >
        fruits
      </li>
      <li
        :class="currentTab === 'crops' && 'border-b-3 border-b-primary'"
        class="cursor-pointer w-24 text-center"
        @click="$emit('changeTab', 'crops')"
      >
        crops
      </li>
      <li
        :class="currentTab === 'vegetables' && 'border-b-3 border-b-primary'"
        class="cursor-pointer w-24 text-center"
        @click="$emit('changeTab', 'vegetables')"
      >
        vegetables
      </li>
    </ul>
  </div>
</template>
<script setup>
const props = defineProps({
  currentTab: String,
});
</script>
