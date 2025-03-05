<template>
  <div>
    <h1 class="text-5xl text-center font-extrabold">
      Expanding new business opportunities <br />
      <span class="font-normal text-3xl">
        while building meaningful connections worldwide
      </span>
    </h1>
    <div
      class="mt-12 group relative overflow-hidden whitespace-nowrap py-10 [mask-image:_linear-gradient(to_right,_transparent_0,_white_128px,white_calc(100%-128px),_transparent_100%)]"
    >
      <div
        class="animate-slide-left-infinite group-hover:animation-pause inline-flex w-max gap-24 px-12"
      >
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/tapu-1.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/tapu-1.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
      </div>

      <div
        class="animate-slide-left-infinite group-hover:animation-pause inline-flex w-max gap-24 px-12"
      >
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="Transistor"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/tapu-1.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/tapu-1.png"
          alt="tapu-foods"
        />
        <img
          class="mx-4 inline h-16 opacity-75"
          src="/images/abicol-logo.png"
          alt="tapu-foods"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.animate-slide-left-infinite {
  animation: slide-left 15s linear infinite;
}
.animation-pause {
  animation-play-state: paused;
}
@keyframes slide-left {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-100%);
  }
}
</style>
