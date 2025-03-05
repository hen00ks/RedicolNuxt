<template>
  <div
    class="py-24 px-4 bg-primary-dark flex flex-col items-center gap-24 text-white"
  >
    <div class="place-items-center">
      <h2 class="header max-w-6xl text-white mb-4">
        Quality Services and Fresh Products Tailored for You
      </h2>
      <p class="max-w-xl text-center font-light opacity-75">
        We provide reliable, end-to-end solutions for sourcing fresh
        agricultural products directly from local farmers to meet your bulk
        needs
      </p>
    </div>
    <div>
      <h3 class="header text-primary-light w-fit pl-8 mb-4">
        Why Work with Us
      </h3>
      <div class="flex flex-wrap justify-center gap-8">
        <div
          v-for="(item, i) in list"
          :key="i"
          class="max-w-96 p-8 space-y-4 font-light place-items-center text-center"
          :class="
            i == 1 && 'border-y-4 border-primary sm:border-y-0 sm:border-x-4'
          "
        >
          <h3 class="text-2xl font-text">
            {{ item.title }}
          </h3>
          <p class="opacity-75">{{ item.desc }}</p>
        </div>
      </div>
    </div>
    <div class="place-items-center space-y-4">
      <p>Explore more about our services</p>
      <Button variant="outline">Services</Button>
    </div>
  </div>
</template>
<script setup>
const list = [
  {
    title: "Direct Sourcing",
    desc: "We partner with trusted local farmers to bring you fresh, high-quality products straight from the source, eliminating third-party involvement",
  },
  {
    title: "Bulk Supply Solutions",
    desc: "We cater to large-scale buyers like universities, hotels, and businesses, ensuring consistent and timely deliveries tailored to your needs",
  },
  {
    title: "Quality Assurance",
    desc: "Every product we deliver undergoes rigorous quality checks to guarantee freshness, cleanliness, and reliability",
  },
];
</script>
