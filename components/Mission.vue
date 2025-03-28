<template>
  <div class="flex flex-wrap gap-16 justify-around items-center px-2">
    <div class="max-w-xl space-y-12">
      <div
        v-for="item in about ? list2 : list"
        class="py-4 space-y-4 not-last:border-b-2 border-b-primary-light"
      >
        <h5 class="header text-primary w-fit" :class="about && 'text-3xl'">
          {{ item.title }}
        </h5>
        <div class="flex gap-4">
          <Icon
            :name="item.icon"
            :size="about ? '100' : '64'"
            class="text-primary"
          />
          <p
            class="italic text-primary-dark sm:text-xl"
            :class="about && 'not-italic whitespace-pre-line !text-lg'"
          >
            {{ item.desc }}
          </p>
        </div>
      </div>
    </div>
    <div class="place-items-center">
      <Circles
        imageUrl="/images/field.png"
        class="mb-8"
        :class="about ? 'block scale-75 origin-center' : 'hidden'"
      />
      <Circles
        imageUrl="/images/truck.png"
        class="mb-8"
        :class="about ? 'block scale-85 origin-center' : 'hidden'"
      />
      <Circles imageUrl="/images/store.png" class="mb-8" />
      <div :class="about && 'hidden'">
        <p>want to know more about us?</p>
        <Button variant="outline">Learn More</Button>
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  about: {
    type: Boolean,
    default: false,
  },
});
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
const list2 = [
  {
    title: "Mission",
    icon: "solar:eye-scan-line-duotone",
    desc: "•	Wholesale high-quality farm and agricultural products to corporate customers, thereby narrowing the prevailing supply chain between producers and end-users/consumers.\n\n•	Creating sustainable, lasting partnership and business networks among farmers and agri-business so as to drive mutual prosperity and economic transformation.",
  },
  {
    title: "Vision",
    icon: "solar:target-line-duotone",
    desc: "•	By 2030, we envision at becoming one of the leading wholesale companies sourcing farm and agricultural products from where they are cultivated and produced.",
  },
  {
    title: "Goal",
    icon: "solar:rocket-line-duotone",
    desc: "•	We aim at developing trusted name as key wholesaler of Ethiopian farm and agricultural products to corporate customers involved in food processing industries such as fast foods providers, hotels and restaurants.",
  },
];
</script>
