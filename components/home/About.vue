<template>
  <div
    class="overflow-x-clip relative bg-[url('/images/crop-bg-removed.png')] bg-cover bg-bottom h-96 w-full flex items-center justify-around p-4"
  >
    <img
      src="/images/crop-bg-croped.png"
      alt=""
      class="crop-image absolute bottom-0 sm:-left-0 -left-42 w-[90%] min-w-4xl"
    />
    <div class="space-y-8 z-10">
      <p class="text-white max-w-2xl">
        At Redicol, we believe in connecting local farmers with universities,
        hotels, and businesses by delivering fresh, high-quality agricultural
        products directly from the source. We aim to bridge the gap between the
        fields and your table with trust and transparency.
      </p>
      <Button variant="outline" color="white">More About Us</Button>
    </div>
    <img src="/images/logo-icon.png" alt="logo" class="w-72" />
  </div>
</template>
<style scoped>
.crop-image {
  transform-origin: bottom;
  animation: scale-up ease-in-out;
  animation-timeline: view();
  animation-range: cover contain;
}
@keyframes scale-up {
  from {
    scale: 0.4;
  }
  to {
    scale: 1;
  }
}
</style>
