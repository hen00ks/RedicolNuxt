<template>
  <div class="flex flex-col gap-16">
    <div class="flex flex-col items-center text-center gap-4">
      <h3 class="header text-xl text-primary">
        Direct from Farmers, Delivered to You.
      </h3>
      <h1 class="header">Freshness Without Compromise</h1>
      <p class="text-primary-dark max-w-3xl w-auto">
        We connect local farmers to universities, hotels, and businesses by
        delivering clean, high-quality agricultural products straight from the
        source
      </p>
      <div class="flex gap-12">
        <Button>Explore our Services</Button>
        <Button variant="outline">Contact us Now</Button>
      </div>
    </div>
    <div class="relative flex flex-col items-center">
      <div class="flex justify-between max-w-7xl w-full px-8 -mb-32">
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
          <img :src="elem.imgUrl" alt="image" />
          <h5
            class="animate-color-change text-primary bg-primary-light font-semibold text-sm py-1 px-3 rounded-full"
          >
            {{ elem.text }}
          </h5>
        </div>
      </div>
      <div class="w-[min(180px,35vw)] -mb-28">
        <img src="/images/geberie.png" alt="farmer image" class="w-full" />
      </div>
      <div class="overflow-x-hidden w-full place-content-center">
        <!-- <img
          src="/images/farm-land.svg"
          alt="farm svg image"
          class="w-[100vw] sm:w-[max(100%,2000px)]"
        /> -->
        <HomeFarmLand
          class="w-[100vw] sm:w-[max(100%,2000px)] place-self-center"
        />
      </div>
    </div>
  </div>
</template>
<script setup>
const fruits = [
  { imgUrl: "/images/apple.png", text: "Sustainability" },
  { imgUrl: "/images/apple.png", text: "Innovation" },
  { imgUrl: "/images/apple.png", text: "Nature" },
  { imgUrl: "/images/apple.png", text: "Energy" },
  { imgUrl: "/images/apple.png", text: "Eco" },
  { imgUrl: "/images/apple.png", text: "Purity" },
];

const crops = [
  { imgUrl: "/images/wheat.png", text: "Growth" },
  { imgUrl: "/images/wheat.png", text: "Balance" },
  { imgUrl: "/images/wheat.png", text: "Organic" },
  { imgUrl: "/images/wheat.png", text: "Breeze" },
  { imgUrl: "/images/wheat.png", text: "Harmony" },
  { imgUrl: "/images/wheat.png", text: "Refresh" },
];

const vegetables = [
  { imgUrl: "/images/spinach.png", text: "Future" },
  { imgUrl: "/images/spinach.png", text: "Bright" },
  { imgUrl: "/images/spinach.png", text: "Green" },
  { imgUrl: "/images/spinach.png", text: "Flow" },
  { imgUrl: "/images/spinach.png", text: "Light" },
  { imgUrl: "/images/spinach.png", text: "Clean" },
];

const dataSet = ref(vegetables);

onMounted(() => {
  let index = 0;
  const dataSets = [fruits, crops, vegetables];

  dataSet.value = dataSets[index];

  setInterval(() => {
    index = (index + 1) % dataSets.length;
    dataSet.value = dataSets[index];
  }, 3000);
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
