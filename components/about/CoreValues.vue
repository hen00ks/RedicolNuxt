<script setup>
import { ref } from "vue";

const coreValues = ref([
  {
    title: "Dependable Quality",
    description:
      "Commitment to delivering the highest standards in products and services, ensuring customer satisfaction and trust",
    icon: "solar:medal-ribbons-star-bold-duotone",
  },
  {
    title: "Integrity",
    description:
      "Maintaining honesty, transparency, and accountability in all business dealings",
    icon: "solar:shield-check-bold-duotone",
  },
  {
    title: "Focus on Customer Needs",
    description:
      "Prioritizing customer needs and exceeding expectations through exceptional service and product offerings",
    icon: "solar:user-hand-up-bold-duotone",
  },
  {
    title: "Innovation",
    description:
      "Embracing new ideas and technologies to continually improve processes, products, and services",
    icon: "solar:lightbulb-bold-duotone",
  },
  {
    title: "Sustainability",
    description:
      "Promoting environmentally and socially responsible practices to support continuing long-term well-being",
    icon: "solar:leaf-bold-duotone",
  },
  {
    title: "Teamwork",
    description:
      "Fostering collaboration and mutual respect among employees, partners, and stakeholders to achieve shared goals",
    icon: "solar:users-group-rounded-bold-duotone",
  },
  {
    title: "Reliability",
    description:
      "Ensuring consistency in quality delivery and performance to build lasting relationships with clients and partners",
    icon: "solar:clock-circle-bold-duotone",
  },
  {
    title: "Empowering Collaboration",
    description:
      "Collaborating and working together with local producers, businesses and employees, contributing to collective economic development.",
    icon: "solar:hand-stars-bold-duotone",
  },
]);
</script>

<template>
  <div id="core-values" class="container mx-auto px-4 py-12">
    <h2 class="header text-primary-dark mb-12 text-center">CORE VALUES</h2>

    <div
      class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 max-w-7xl mx-auto"
    >
      <div
        v-for="(value, index) in coreValues"
        :key="index"
        class="core-value-card border-2 border-primary-light rounded-xl p-6 transition-all duration-300 hover:border-primary hover:shadow-lg hover:-translate-y-1 bg-white flex flex-col items-center text-center h-full"
      >
        <Icon
          :name="value.icon"
          size="48"
          class="text-primary mb-4 transition-all duration-300 group-hover:scale-110"
        />
        <h3 class="text-lg font-bold text-primary-dark mb-3">
          {{ value.title }}
        </h3>
        <p class="text-sm text-primary-dark">{{ value.description }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Make Core Values responsive */
@media (max-width: 768px) {
  .core-value-card {
    padding: 1rem;
  }

  h3 {
    font-size: 1.1rem;
  }
}
</style>
