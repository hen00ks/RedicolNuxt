<script setup>
const routes = [
  { path: "/", name: "Home" },
  { path: "/about", name: "About" },
  { path: "/products", name: "Products" },
  { path: "/contact", name: "Contact" },
];
</script>
<template>
  <header
    class="flex justify-between px-16 py-5 mb-16 border-b-2 border-primary-light"
  >
    <div class="h-14">
      <img
        src="/images/logo.png"
        alt="Redicol logo"
        class="size-full object-contain"
      />
    </div>
    <nav class="hidden items-center gap-16 text-primary-dark sm:flex">
      <NuxtLink
        v-for="route in routes"
        :to="route.path"
        :key="route.name"
        activeClass="font-bold"
        >{{ route.name }}</NuxtLink
      >
    </nav>
    <nav
      class="fixed bg-amber-200 w-screen left-0 bottom-0 flex justify-between z-50"
    >
      <NuxtLink
        v-for="route in routes"
        :to="route.path"
        :key="route.name"
        activeClass="font-bold"
        class="w-full bg-amber-600 text-center py-4 sm:hidden"
        >{{ route.name }}</NuxtLink
      >
    </nav>
  </header>
</template>
