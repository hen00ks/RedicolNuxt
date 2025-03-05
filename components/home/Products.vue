<script setup></script>

<template>
  <div
    class="max-w-4xl mx-auto flex items-center justify-center sm:justify-between gap-8 sm:gap-24 flex-wrap"
  >
    <div>
      <h3 class="header text-primary w-fit mb-4">What We Offer</h3>
      <img src="/images/coffee-beans.png" alt="" class="w-96" />
    </div>

    <div class="max-w-96">
      <h2 class="header text-start mb-8">From the farm To your table,</h2>
      <p>
        we offer a wide variety of fresh agricultural products to meet your
        business needs
      </p>
    </div>
  </div>
  <div class="flex flex-wrap justify-center gap-12">
    <div class="w-fit">
      <Circles class="top-circle scale-64" imageUrl="/images/crops.png" />
      <h2 class="header text-stroke">Crops</h2>
    </div>
    <div class="w-fit">
      <Circles class="top-circle scale-64" imageUrl="/images/fruits.png" />
      <h2 class="header text-stroke">Fruits</h2>
    </div>
    <div class="w-fit group">
      <Circles
        class="top-circle scale-64 group-hover:translate-y-6 transition-transform duration-1000"
        imageUrl="/images/vegetables.png"
      />
      <h2 class="header text-stroke">Vegetables</h2>
    </div>
  </div>
</template>

<style scoped>
.text-stroke {
  color: white;
  text-shadow: 1px 1px 0 var(--color-primary-dark),
    /* right-bottom */ -1px 1px 0 var(--color-primary-dark),
    /* left-bottom */ 1px -1px 0 var(--color-primary-dark),
    /* right-top */ -1px -1px 0 var(--color-primary-dark),
    /* left-top */ 1px 0 0 var(--color-primary-dark),
    /* right */ -1px 0 0 var(--color-primary-dark),
    /* left */ 0 1px 0 var(--color-primary-dark),
    /* bottom */ 0 -1px 0 var(--color-primary-dark); /* top */
}

.top-circle {
  animation: translate-up 1s ease-out;
  animation-timeline: view();
  animation-range-end: contain;
  animation-range-start: entry;
}

@keyframes translate-up {
  from {
    transform: translateY(500px);
    scale: 0.5;
  }
  to {
    transform: translateY(0);
    /* scale: 0.65; */
  }
}
</style>
