<script setup>
const props = defineProps({
  header: String,
});

const fruits = [
  { src: "/images/peach.png", name: "ፖም" },
  { src: "/images/banana.png", name: "ሙዝ" },
  { src: "/images/mango.png", name: "ማንጎ" },
  { src: "/images/lemon.png", name: "ሎሚ" },
  { src: "/images/watermelon.png", name: "ሀብሀብ" },
  { src: "/images/strawberry.png", name: "እንጆሪ" },
  { src: "/images/wine.png", name: "የወይን ፍሬ" },
  { src: "/images/orange.png", name: "ብርቱካን" },
];

const crops = [
  { src: "/images/crop.png", name: "ስንዴ" },
  { src: "/images/ricee.png", name: "ሩዝ" },
  { src: "/images/corn.png", name: "በቆሎ" },
  { src: "/images/beans.png", name: "ባቄላ" },
  { src: "/images/lentils.png", name: "ምስር" },
  { src: "/images/teff.png", name: "ጤፍ" },
  { src: "/images/pea.png", name: "አተር" },
  { src: "/images/fosolia.png", name: "ፎሶሊያ" },
];

const vegetables = [
  { src: "/images/tomato.png", name: "ቲማቲም" },
  { src: "/images/onion.png", name: "ሽንኩርት" },
  { src: "/images/garlic.png", name: "ነጭ ሽንኩርት" },
  { src: "/images/cabbage.png", name: "ጥቅል ጎመን" },
  { src: "/images/broccoli.png", name: "የአበባ ጎመን" },
  { src: "/images/cucumber.png", name: "ኪያር" },
  { src: "/images/pumpkin.png", name: "ዱባ" },
  { src: "/images/green.png", name: "ጎመን" },
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
