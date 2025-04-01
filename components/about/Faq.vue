<script setup>
import { ref } from "vue";

const faqs = ref([
  {
    question: "What products does Redicol Trading PLC offer?",
    answer:
      "Redicol offers a diverse range of farm-fresh agricultural products including fruits, vegetables, grains, and pulses, as well as imported kitchen appliances, food packaging materials, and facilities tailored for corporate customers.",
    isOpen: false,
  },
  {
    question: "How does Redicol ensure product quality?",
    answer:
      "We maintain strict quality control measures by working directly with trusted farmers and suppliers, conducting regular inspections, and implementing proper handling and storage practices to ensure freshness and quality from farm to delivery.",
    isOpen: false,
  },
  {
    question: "What is Redicol's relationship with farmers?",
    answer:
      "Redicol builds sustainable partnerships with local farmers, offering fair compensation and long-term business relationships. We work closely with agricultural communities to support their growth while ensuring consistent supply of high-quality products.",
    isOpen: false,
  },
  {
    question: "How does Redicol contribute to sustainability?",
    answer:
      "By shortening the supply chain between producers and end-users, we reduce food waste and transportation emissions. We also promote sustainable farming practices among our partner farmers and implement eco-friendly packaging solutions where possible.",
    isOpen: false,
  },
  {
    question: "Who are Redicol's sister companies?",
    answer:
      "Redicol works closely with TAPU FOODS, our sister company specializing in packed food products, and Abicol Import Export PLC, which focuses on exporting Ethiopian agricultural products to international markets.",
    isOpen: false,
  },
  {
    question: "How can businesses become Redicol customers?",
    answer:
      "Corporate customers interested in our wholesale agricultural products or imported kitchen appliances can contact us through our website, email, or phone. Our team will work with you to understand your specific needs and create a customized supply solution.",
    isOpen: false,
  },
]);

const toggleFaq = (index) => {
  faqs.value[index].isOpen = !faqs.value[index].isOpen;
};
</script>

<template>
  <div id="faq" class="container mx-auto px-4 py-12">
    <h2 class="header text-primary-dark mb-12">FAQs</h2>

    <div class="max-w-3xl mx-auto">
      <div
        v-for="(faq, index) in faqs"
        :key="index"
        class="mb-4 border border-primary-light rounded-xl overflow-hidden transition-all duration-300"
        :class="{ 'border-primary': faq.isOpen }"
      >
        <button
          @click="toggleFaq(index)"
          class="w-full flex justify-between items-center p-5 text-left bg-white hover:bg-primary-light/20 transition-colors duration-300"
          :class="{ 'bg-primary-light/20': faq.isOpen }"
        >
          <h3 class="text-lg font-bold text-primary-dark">
            {{ faq.question }}
          </h3>
          <Icon
            :name="
              faq.isOpen
                ? 'solar:minus-circle-line-duotone'
                : 'solar:add-circle-line-duotone'
            "
            size="24"
            class="text-primary transition-transform duration-300"
          />
        </button>

        <div
          class="overflow-hidden transition-all duration-300 bg-white"
          :class="faq.isOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <p class="p-5 text-sm text-primary-dark">{{ faq.answer }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Make FAQ responsive */
@media (max-width: 768px) {
  h3 {
    font-size: 1.1rem;
  }

  button {
    padding: 1rem;
  }

  p {
    padding: 1rem;
  }
}
</style>
