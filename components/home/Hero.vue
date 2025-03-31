<template>
  <div class="flex flex-col gap-16">
    <div class="flex flex-col items-center text-center gap-4">
      <h3 class="header text-xl text-yellow-600">
        Direct from Farmers,<br class="sm:hidden" />
        Delivered to You
      </h3>
      <h1 class="header">Freshness Without Compromise</h1>
      <p class="text-primary-dark max-w-3xl w-auto">
        Facilitating direct farm-to-business distribution, supplying fresh
        agricultural products to companies, hotels, and institutions
      </p>
      <div class="flex flex-wrap gap-4 sm:gap-12 justify-center">
        <NuxtLink to="/products"
          ><Button>Explore our Products</Button></NuxtLink
        >
        <NuxtLink to="/contact">
          <Button variant="outline">Contact us Now</Button></NuxtLink
        >
      </div>
    </div>
    <div class="relative flex flex-col items-center overflow-x-clip">
      <div class="flex justify-between max-w-7xl sm:w-full px-8 -mb-32">
        <div
          v-for="(elem, i) in dataSet"
          :class="
            i === 0 || i === 5
              ? 'mt-32 opacity-0 scale-0 sm:opacity-100 sm:scale-100'
              : i === 1 || i === 4
              ? 'mt-16'
              : 'mt-0'
          "
          class="animate-fade-in-out-y size-20 flex flex-col items-center justify-center"
        >
          <img
            :src="elem.imgUrl"
            alt="image"
            class="size-12 object-cover rounded-full"
          />
          <h5
            class="animate-color-change text-primary bg-primary-light font-semibold text-sm py-1 px-3 rounded-full"
          >
            {{ elem.text }}
          </h5>
        </div>
      </div>
      <!-- gebere -->
      <div class="-mb-28 z-10">
        <NuxtImg width="150" src="/images/geberie.png" alt="farmer image" />
      </div>
      <!-- svg -->
      <div class="overflow-x-clip w-full place-content-center z-20">
        <HomeFarmLand class="w-[max(100%,2000px)] place-self-center" />
      </div>
    </div>
  </div>
</template>
<script setup>
const fruits = [
  { imgUrl: "/images/mango.png", text: "Sustainability" },
  { imgUrl: "/images/apple.png", text: "Innovation" },
  { imgUrl: "/images/banana.png", text: "Nature" },
  { imgUrl: "/images/wine.png", text: "Energy" },
  { imgUrl: "/images/watermelon.png", text: "Eco" },
  { imgUrl: "/images/pineapple.png", text: "Purity" },
];

const crops = [
  { imgUrl: "/images/boloqe.png", text: "Growth" },
  { imgUrl: "/images/corn.png", text: "Balance" },
  { imgUrl: "/images/wheat.png", text: "Organic" },
  { imgUrl: "/images/rice.png", text: "Breeze" },
  { imgUrl: "/images/beans.png", text: "Harmony" },
  { imgUrl: "/images/lentils.png", text: "Refresh" },
];

const vegetables = [
  { imgUrl: "/images/garlic.png", text: "Future" },
  { imgUrl: "/images/tomato.png", text: "Bright" },
  { imgUrl: "/images/broccoli.png", text: "Green" },
  { imgUrl: "/images/spinach.png", text: "Flow" },
  { imgUrl: "/images/cucumber.png", text: "Light" },
  { imgUrl: "/images/fosolia.png", text: "Clean" },
];

const dataSet = ref(vegetables);

onMounted(() => {
  let index = 0;
  const dataSets = [fruits, crops, vegetables];

  dataSet.value = dataSets[index];

  setInterval(() => {
    index = (index + 1) % dataSets.length;
    dataSet.value = dataSets[index];
  }, 5000);
});
</script>
<!-- <style scoped>
.animate {
  animation: change 9s infinite;
}

.animate :last-child {
  animation: colorChange 9s infinite;
  color: var(--color-primary);
  background-color: var(--color-primary-light);
}

@keyframes change {
  6.6% {
    opacity: 0;
    transform: translateY(20px);
  }
  33.3% {
    opacity: 1;
    transform: translateY(0px);
  }
  40% {
    opacity: 0;
    transform: translateY(20px);
  }
  66.6% {
    opacity: 1;
    transform: translateY(0px);
  }
  73.3% {
    opacity: 0;
    transform: translateY(20px);
  }
}

@keyframes colorChange {
  33.3% {
    color: var(--color-blue-700);
    background-color: var(--color-blue-100);
  }
  66.6% {
    color: var(--color-red-700);
    background-color: var(--color-red-100);
  }
}
</style> -->
