<template>
  <div class="container mx-auto px-4 py-12 scale-90">
    <div class="relative">
      <!-- Timeline line -->
      <h2 class="header mb-12">{{ title }}</h2>
      <div
        class="absolute left-1/2 transform -translate-x-1/2 h-full w-0.5 bg-gradient-to-b to-primary via-primary-light from-primary-dark"
      ></div>

      <!-- Timeline items -->
      <div class="relative">
        <div v-for="(item, index) in timelineItems" :key="index" class="mb-16">
          <!-- Content container with alternating sides -->
          <div class="flex items-center justify-center">
            <!-- Left side content (even indexes) -->
            <div
              v-if="index % 2 === 0"
              class="w-1/2 pr-12 text-right relative group"
            >
              <div
                class="bg-white p-6 rounded-xl border border-gray-100 relative cursor-pointer inline-block transition-all duration-300 hover:border-primary-light hover:translate-y-[-2px]"
                @mouseenter="activeItem = index"
                @mouseleave="activeItem = null"
              >
                <span
                  class="text-xs font-medium text-primary uppercase tracking-wider mb-1 block"
                  >{{ item.date }}</span
                >
                <h3 class="text-xl font-bold mb-2">
                  {{ item.title }}
                </h3>
                <p class="text-gray-500">{{ item.description }}</p>

                <!-- Floating image -->
                <div
                  v-show="activeItem === index"
                  class="hidden md:block absolute z-10 left-full ml-8 transform transition-all duration-300 ease-out opacity-0 group-hover:opacity-100"
                  :class="{
                    'translate-x-[-20px] group-hover:translate-x-0':
                      activeItem === index,
                  }"
                >
                  <img
                    :src="item.image"
                    :alt="item.title"
                    class="rounded-lg border border-gray-100 max-w-[250px] shadow-[0_10px_40px_-15px_rgba(0,0,0,0.1)]"
                    loading="lazy"
                  />
                </div>
              </div>
            </div>

            <!-- Center dot -->
            <div
              class="z-10 flex-shrink-0 w-5 h-5 rounded-full bg-gradient-to-r from-primary-light to-primary border-4 border-white shadow-md transform transition-all duration-300"
              :class="{ 'scale-125': activeItem === index }"
            ></div>

            <!-- Right side content (odd indexes) -->
            <div v-if="index % 2 !== 0" class="w-1/2 pl-12 relative group">
              <div
                class="bg-white p-6 rounded-xl border border-gray-100 relative cursor-pointer inline-block transition-all duration-300 hover:border-primary-light hover:translate-y-[-2px]"
                @mouseenter="activeItem = index"
                @mouseleave="activeItem = null"
              >
                <span
                  class="text-xs font-medium text-primary uppercase tracking-wider mb-1 block"
                  >{{ item.date }}</span
                >
                <h3 class="text-xl font-bold mb-2 text-gray-800">
                  {{ item.title }}
                </h3>
                <p class="text-gray-500">{{ item.description }}</p>

                <!-- Floating image -->
                <div
                  v-show="activeItem === index"
                  class="hidden md:block absolute z-10 right-full mr-8 transform transition-all duration-300 ease-out opacity-0 group-hover:opacity-100"
                  :class="{
                    'translate-x-[20px] group-hover:translate-x-0':
                      activeItem === index,
                  }"
                >
                  <img
                    :src="item.image"
                    :alt="item.title"
                    class="rounded-lg border border-gray-100 max-w-[250px] shadow-[0_10px_40px_-15px_rgba(0,0,0,0.1)]"
                    loading="lazy"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
defineProps(["timelineItems", "title"]);
const activeItem = ref(null);
</script>

<style scoped>
/* Make timeline responsive */
@media (max-width: 768px) {
  .flex {
    flex-direction: column;
  }

  .w-1\/2 {
    width: 100%;
    padding: 0 0 0 2.5rem !important;
    text-align: left !important;
    margin-bottom: 1.5rem;
  }

  .absolute.left-1\/2 {
    left: 1.25rem;
  }

  .z-10.flex-shrink-0 {
    position: absolute;
    left: 1.25rem;
    margin-top: 1.5rem;
  }

  .group .absolute.z-10 {
    position: relative !important;
    left: 0 !important;
    right: 0 !important;
    margin: 1rem 0 0 0 !important;
    transform: none !important;
    opacity: 1 !important;
  }

  .group .absolute.z-10 img {
    max-width: 100% !important;
  }
}

.group:hover {
  z-index: 10;
}
</style>
