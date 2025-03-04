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
      <div class="flex justify-between w-full px-4 -mb-32">
        <div
          v-for="(_, i) in Array(6)"
          :class="
            i === 0 || i === 5 ? 'mt-32' : i === 1 || i === 4 ? 'mt-16' : 'mt-0'
          "
          class="size-20 flex items-center justify-center outline"
        >
          icon {{ i }}
        </div>
      </div>
      <div class="w-[min(180px,35vw)] -mb-28">
        <img src="/images/geberie.png" alt="farmer image" class="w-full" />
      </div>
      <div class="overflow-x-hidden w-full place-content-center">
        <img
          src="/images/farm-land.svg"
          alt="farm svg image"
          class="w-[100vw] sm:w-[max(100%,2000px)]"
        />
      </div>
    </div>
  </div>
</template>
