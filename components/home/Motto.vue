<template>
  <div
    class="flex items-center place-self-center justify-between w-full overflow-x-clip"
  >
    <Circles class="hidden sm:block -translate-x-1/2" />
    <div class="place-items-center space-y-4">
      <div class="relative">
        <h1 class="header pl-8">
          <span class="relative"
            >Rooted
            <img
              src="/images/root.svg"
              class="absolute -left-12.5 sm:top-14 top-10 -z-10 sm:scale-115"
            />
          </span>
          in Quality
        </h1>
      </div>
      <div class="relative">
        <h2 class="header not-sm:text-3xl pl-8">
          <span class="relative"
            ><img
              src="/images/drive.svg"
              class="absolute sm:-left-7.5 -left-6 sm:top-4.5 top-2 scale-80 sm:scale-110"
            />Driven</span
          >
          by Purpose
        </h2>
      </div>
    </div>
    <Circles class="hidden sm:block translate-x-1/2" />
  </div>
</template>
