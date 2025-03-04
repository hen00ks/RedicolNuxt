<template>
  <div class="overflow-x-clip">
    <div class="flex items-center place-self-center justify-between w-[120vw]">
      <Circles />
      <div class="place-items-center space-y-4">
        <div class="relative">
          <h1 class="header">Rooted in Quality</h1>
          <img
            src="/images/root.svg"
            class="absolute sm:-left-12.5 left-2 sm:top-12 top-9 -z-10 sm:scale-110"
          />
        </div>
        <div class="relative">
          <h2 class="header">Driven by Purpose</h2>
          <img
            src="/images/drive.svg"
            class="absolute sm:-left-7.5 -left-6 sm:top-4.5 top-2 scale-75 sm:scale-100"
          />
        </div>
      </div>
      <Circles />
    </div>
  </div>
</template>
