<script setup>
import {
  IconsHome,
  IconsAbout,
  IconsProducts,
  IconsContact,
  IconsMenu,
} from "#components";
const routes = [
  { path: "/", name: "Home", icon: IconsHome },
  { path: "/about", name: "About", icon: IconsAbout },
  { path: "/products", name: "Products", icon: IconsProducts },
  { path: "/contact", name: "Contact", icon: IconsContact },
];
const showNav = ref(false);
</script>
<template>
  <header
    class="flex justify-center px-16 py-2 mb-16 border-b-2 border-primary-light"
  >
    <NuxtImg
      src="/images/logo.png"
      height="56"
      alt="Redicol logo"
      class="h-14 object-contain -translate-x-2 sm:-translate-x-0"
    />
    <!-- desktop menu -->
    <nav class="hidden sm:flex ml-auto items-center gap-16 text-primary-dark">
      <NuxtLink
        v-for="route in routes"
        :to="route.path"
        :key="route.name"
        activeClass="font-bold"
        >{{ route.name }}</NuxtLink
      >
    </nav>
    <!-- mobile menu -->
    <nav
      :class="showNav ? 'translate-y-0' : 'translate-y-full opacity-50'"
      class="sm:hidden bg-yellow-600 fixed w-screen left-0 bottom-0 z-50 py-2 flex justify-between text-primary-dark transition-all duration-500"
    >
      <NuxtLink
        v-for="route in routes"
        :to="route.path"
        :key="route.name"
        activeClass="font-bold text-white/90"
        class="w-full text-center text-sm place-items-center"
      >
        <component :is="route.icon" class="size-6" />
        {{ route.name }}</NuxtLink
      >
    </nav>
    <button
      class="fixed sm:hidden right-0 bottom-24 size-14 pl-4 rounded-l-full bg-white/90 shadow-lg z-50 active:bg-white/60 active:scale-95"
      @click="showNav = !showNav"
    >
      <IconsClose v-if="showNav" class="size-8" />
      <IconsMenu v-else class="size-8" />
    </button>
  </header>
</template>
