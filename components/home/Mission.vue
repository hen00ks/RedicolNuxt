<template>
  <div class="flex flex-wrap gap-16 justify-around">
    <div class="max-w-xl">
      <div
        v-for="item in list"
        class="py-4 space-y-4 not-last:border-b-2 border-b-primary-light"
      >
        <h5 class="header text-primary w-fit">
          {{ item.title }}
        </h5>
        <div class="flex gap-4">
          <Icon :name="item.icon" size="64" class="text-primary" />
          <p class="italic text-primary-dark text-xl">{{ item.desc }}</p>
        </div>
      </div>
    </div>
    <div class="place-items-center">
      <Circles imageUrl="/images/coffee-beans.png" class="mb-8" />
      <p>want to know more about us?</p>
      <Button variant="outline">Learn More</Button>
    </div>
  </div>
</template>
<script setup>
const list = [
  {
    title: "Mission",
    icon: "solar:eye-scan-line-duotone",
    desc: "Empowering farmers, elevating quality, and building trust in every delivery.",
  },
  {
    title: "Vision",
    icon: "solar:target-line-duotone",
    desc: "To redefine agricultural supply chains with freshness, sustainability, and direct partnerships.",
  },
  {
    title: "Goal",
    icon: "solar:rocket-line-duotone",
    desc: "Delivering excellence to our clients while ensuring fair opportunities for local farmers.",
  },
];
</script>
