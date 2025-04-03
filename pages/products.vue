<script setup>
const currentTab = ref("fruits");

const processSteps = [
  {
    title: "Initial Consultation",
    description:
      "Schedule a meeting with our team to discuss your agricultural needs, product requirements, and business goals.",
    date: "Step 1",
    image: "/images/office.png",
  },
  {
    title: "Product Selection",
    description:
      "Browse our extensive catalog of fruits, vegetables, and crops. Our experts will help you select the best products for your market.",
    date: "Step 2",
    image: "/images/fruits.png",
  },
  {
    title: "Quality Inspection",
    description:
      "Visit our facilities to inspect product quality or request sample shipments to ensure our products meet your standards.",
    date: "Step 3",
    image: "/images/field.png",
  },
  {
    title: "Contract Agreement",
    description:
      "Finalize terms, pricing, delivery schedules, and payment methods with our business team to establish a clear partnership framework.",
    date: "Step 4",
    image: "/images/store.png",
  },
  {
    title: "Delivery & Ongoing Support",
    description:
      "Receive your products on schedule with our reliable logistics network, and enjoy continuous support from our dedicated customer service team.",
    date: "Step 5",
    image: "/images/truck.png",
  },
];
</script>

<template>
  <div class="place-items-center space-y-40">
    <ProductsHistory />
    <div>
      <ProductsTab :currentTab @changeTab="(tab) => (currentTab = tab)" />
      <ProductsImages :header="currentTab" />
    </div>
    <Processes :timelineItems="processSteps" title="How to Work With Us" />
  </div>
</template>
