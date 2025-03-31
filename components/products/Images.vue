<script setup>
const props = defineProps({
  header: String,
});

const fruits = [
  { src: "/images/peach.png", name: "Peach" },
  { src: "/images/banana.png", name: "Banana" },
  { src: "/images/mango.png", name: "Mango" },
  { src: "/images/pineapple.png", name: "Pineapple" },
  { src: "/images/watermelon.png", name: "Watermelon" },
  { src: "/images/avocado.png", name: "Avocado" },
  { src: "/images/wine.png", name: "Wine" },
  { src: "/images/fruits.png", name: "Mixed Fruits" },
];

const crops = [
  { src: "/images/wheat.png", name: "Wheat" },
  { src: "/images/rice.png", name: "Rice" },
  { src: "/images/corn.png", name: "Corn" },
  { src: "/images/beans.png", name: "Beans" },
  { src: "/images/lentils.png", name: "Lentils" },
  { src: "/images/coffee-beans.png", name: "Coffee Beans" },
  { src: "/images/crops.png", name: "Mixed Crops" },
  { src: "/images/fosolia.png", name: "Fosolia" },
];

const vegetables = [
  { src: "/images/tomato.png", name: "Tomato" },
  { src: "/images/onion.png", name: "Onion" },
  { src: "/images/garlic.png", name: "Garlic" },
  { src: "/images/cabbage.png", name: "Cabbage" },
  { src: "/images/broccoli.png", name: "Broccoli" },
  { src: "/images/cucumber.png", name: "Cucumber" },
  { src: "/images/pumpkin.png", name: "Pumpkin" },
  { src: "/images/spinach.png", name: "Spinach" },
];

const images = ref(crops);

watchEffect(() => {
  if (props.header?.toLowerCase().includes("fruit")) {
    images.value = fruits;
  } else if (props.header?.toLowerCase().includes("crop")) {
    images.value = crops;
  } else if (props.header?.toLowerCase().includes("vegetable")) {
    images.value = vegetables;
  }
});
</script>
<template>
  <div class="space-y-4 max-w-7xl place-self-center place-items-center">
    <h2 class="header">{{ header }}</h2>
    <div
      class="px-2 parent w-full grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4"
    >
      <!-- Row 1 -->
      <div
        class="relative aspect-square group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[0].name }}</p>
        </div>
        <NuxtImg
          :src="images[0].src"
          :alt="images[0].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
      <div
        class="md:col-span-2 relative group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[1].name }}</p>
        </div>
        <NuxtImg
          :src="images[1].src"
          :alt="images[1].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
      <div
        class="relative aspect-square group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[2].name }}</p>
        </div>
        <NuxtImg
          :src="images[2].src"
          :alt="images[2].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
      <div
        class="md:col-span-2 relative group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[3].name }}</p>
        </div>
        <NuxtImg
          :src="images[3].src"
          :alt="images[3].name"
          height="200"
          class="size-full object-contain"
        />
      </div>

      <!-- Row 2 -->
      <div
        class="md:col-span-2 relative group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[4].name }}</p>
        </div>
        <NuxtImg
          :src="images[4].src"
          :alt="images[4].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
      <div
        class="relative aspect-square group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[5].name }}</p>
        </div>
        <NuxtImg
          :src="images[5].src"
          :alt="images[5].name"
          height="200"
          class="size-full object-contain"
        />
      </div>

      <div
        class="md:col-span-2 relative group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[6].name }}</p>
        </div>
        <NuxtImg
          :src="images[6].src"
          :alt="images[6].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
      <div
        class="relative aspect-square group hover:scale-105 transition-transform duration-300"
      >
        <div
          class="absolute size-full bg-primary-dark/50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity"
        >
          <p class="text-white">{{ images[7].name }}</p>
        </div>
        <NuxtImg
          :src="images[7].src"
          :alt="images[7].name"
          height="200"
          class="size-full object-contain"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.parent > div {
  border-radius: var(--radius-xl);
  overflow: clip;
  max-height: calc(48px * 4);
  --tw-shadow: 0 25px 50px -12px var(--tw-shadow-color, rgb(0 0 0 / 0.25));
  box-shadow: var(--tw-inset-shadow), var(--tw-inset-ring-shadow),
    var(--tw-ring-offset-shadow), var(--tw-ring-shadow), var(--tw-shadow);
  background-color: #fff;
}
</style>
