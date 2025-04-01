<template>
  <NuxtLink
    :to="to"
    :target="isExternal ? '_blank' : ''"
    class="relative group flex items-center gap-2"
  >
    <span class="group-hover:text-primary-dark flex-1">{{ title }}</span>

    <div v-if="from === 'center'">
      <span
        class="absolute -bottom-1 left-1/2 w-0 transition-all h-0.5 bg-primary-dark group-hover:w-3/6"
      />
      <span
        class="absolute -bottom-1 right-1/2 w-0 transition-all h-0.5 bg-primary-dark group-hover:w-3/6"
      />
    </div>

    <span
      v-else
      class="absolute w-0 bottom-0 transition-all h-0.5 bg-primary-dark group-hover:w-full"
      :class="from === 'right' ? 'right-0' : 'left-0'"
    />

    <component
      v-if="icon"
      :is="icon"
      class="transition-transform group-hover:text-primary-dark group-hover:scale-125"
      :class="{
        'md:scale-90': ['tapu foods', 'abicol', 'see more'].includes(
          title.toLowerCase()
        ),
        'md:scale-0': !['tapu foods', 'abicol', 'see more'].includes(
          title.toLowerCase()
        ),
      }"
    />
  </NuxtLink>
</template>

<script setup>
const props = defineProps({
  title: String,
  to: String,
  from: {
    type: String,
    default: "left",
  },
  icon: [Object, Function],
});
const isExternal = computed(
  () => typeof props.to === "string" && /^https?:\/\//.test(props.to)
);
</script>
