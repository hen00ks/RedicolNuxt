<script setup lang="ts">
import { IconsLink } from "#components";
const { phone, phone2, email, tapuWebsite, abicolWebsite } = useCompanyInfo();
</script>

<template>
  <div class="place-items-center place-self-center px-4 max-w-7xl w-full">
    <div class="justify-center gap-16 items-center flex flex-wrap">
      <div
        class="w-64 px-4 box-content flex-col justify-start items-center gap-7 flex"
      >
        <h3 class="header text-2xl text-nowrap">Tapu Foods</h3>
        <img
          class="size-64 object-cover rounded-t-3xl rounded-br-3xl shadow-2xl"
          src="/images/tapu-logo.png"
        />
        <div class="w-full text-primary text-center font-bold text-nowrap">
          Our packed food supplier
        </div>

        <div class="text-custom-orange">
          <HoverLink
            title="visit website"
            :to="tapuWebsite"
            :icon="IconsLink"
            from="right"
          />
        </div>
      </div>
      <div
        class="w-64 px-4 box-content flex-col justify-center items-center gap-7 flex"
      >
        <h3 class="header text-2xl text-nowrap">Abicol Import Export Plc</h3>
        <div class="size-64 shadow-2xl rounded-t-3xl rounded-br-3xl">
          <img
            class="size-64 object-contain scale-60"
            src="/images/abicol-logo.png"
          />
        </div>
        <div class="text-primary text-center font-bold text-nowrap">
          Our agricultural products exporter
        </div>
        <div class="text-custom-orange">
          <HoverLink
            title="visit website"
            :to="abicolWebsite"
            :icon="IconsLink"
            from="right"
          />
        </div>
      </div>
    </div>
  </div>
</template>
