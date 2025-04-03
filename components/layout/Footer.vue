<script setup>
import {
  IconsFacebook,
  IconsInstagram,
  IconsLink,
  IconsTiktok,
  IconsTelegram,
  IconsWhatsapp,
} from "#components";

const route = useRoute();
const {
  phone,
  phone2,
  email,
  instagram,
  tiktok,
  telegram,
  facebook,
  tapuWebsite,
  abicolWebsite,
} = useCompanyInfo();

const isContactPage = computed(() => route.path === "/contact");
const isHomePage = computed(() => route.path === "/");
</script>

<template>
  <div class="overflow-x-hidden place-items-center">
    <svg
      width="1512"
      height="179"
      viewBox="0 0 1512 179"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M-217 154.928C-150.277 126.157 -65.6648 114.899 7.81622 127.794C89.1397 142.066 169.766 166.194 253.924 156.954C299.688 151.929 342.358 138.105 383.867 121.451C419.905 106.992 458.472 89.1935 499.719 90.7942C537.366 92.2552 575.829 114.625 606.804 130.966C632.466 144.503 658.266 158.187 686.753 167.173C736.203 182.772 792.791 177.734 842.788 166.38C905.129 152.222 954.007 117.99 1005.09 86.7418C1055.14 56.1218 1109.01 25.693 1168.11 9.30619C1208.56 -1.90584 1250.95 -0.775029 1288.56 16.6181C1327.64 34.6936 1359.08 61.0916 1396.17 81.5442C1435.46 103.215 1483.83 105.198 1529.45 104.361C1554.9 103.894 1581.68 101.036 1606.89 105.418C1629.3 109.312 1645.25 120.962 1662 133.256"
        stroke="#2955A5"
        stroke-opacity="0.1"
        stroke-width="3"
        stroke-linecap="round"
      />
    </svg>
    <contactMap v-if="isContactPage" />
    <div v-else class="w-full py-10 text-gray-700">
      <div class="mx-auto max-w-6xl px-4 flex flex-col md:flex-row gap-10">
        <div class="flex flex-col gap-8">
          <img
            class="w-20 saturate-0 brightness-30"
            src="/images/logo-icon.png"
            alt="Logo"
          />
          <div class="flex flex-col gap-4 text-primary-dark font-medium">
            <div class="flex justify-between w-full gap-4">
              <span>{{ phone }}</span>
              <span>{{ phone2 }}</span>
            </div>
            <span>{{ email }}</span>
          </div>
        </div>
        <div
          class="w-full flex justify-between md:justify-end md:gap-24 text-sm sm:text-base"
        >
          <div class="flex flex-col gap-8">
            <div class="text-base font-bold uppercase">Pages</div>
            <div class="flex flex-col justify-start items-start gap-4">
              <HoverLink
                v-for="page in [
                  { title: 'Home', link: '/' },
                  { title: 'About Us', link: '/about' },
                  { title: 'Products', link: '/products' },
                  { title: 'Contact', link: '/contact' },
                ]"
                :key="page.link"
                :title="page.title"
                :to="page.link"
              />
            </div>
          </div>
          <div class="flex flex-col gap-8">
            <div class="text-base font-bold uppercase">Social Media</div>
            <div class="flex-col justify-start items-center gap-4 flex">
              <HoverLink
                v-for="social in [
                  {
                    title: 'Telegram',
                    link: telegram,
                    icon: IconsTelegram,
                  },
                  {
                    title: 'Tiktok',
                    link: tiktok,
                    icon: IconsTiktok,
                  },
                  {
                    title: 'Instagram',
                    link: instagram,
                    icon: IconsInstagram,
                  },
                  {
                    title: 'Facebook',
                    link: facebook,
                    icon: IconsFacebook,
                  },
                  {
                    title: 'WhatsApp',
                    link: 'https://api.whatsapp.com/send/?phone=%2B251963011116',
                    icon: IconsWhatsapp,
                  },
                ]"
                :key="social.link"
                :title="social.title"
                :to="social.link"
                :icon="social.icon"
                from="center"
              />
            </div>
          </div>
          <div class="flex-col justify-start items-end gap-8 inline-flex">
            <div class="text-base font-bold uppercase">Other</div>
            <div class="flex-col justify-start items-end gap-4 flex">
              <HoverLink
                v-for="other in [
                  { title: 'FAQ', link: '/about#faq' },
                  {
                    title: 'Abicol',
                    link: abicolWebsite,
                    icon: IconsLink,
                  },
                  {
                    title: 'Tapu Foods',
                    link: tapuWebsite,
                    icon: IconsLink,
                  },
                ]"
                :key="other.link"
                :title="other.title"
                :to="other.link"
                :icon="other.icon"
                from="right"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="place-self-center p-4">All rights reserved ©️2025 G.C</div>
    <div
      :class="isHomePage ? 'flex' : 'hidden'"
      class="place-self-center p-4 pb-4 gap-2 items-center w-full justify-center md:justify-start border-t-2 text-gray-800/50"
    >
      <p class="text-xs">Designed and Developed by</p>
      <div class="font-semibold text-base">
        <HoverLink to="https://henooksportfolio.netlify.app" title="Henooks" />
      </div>
      <div class="size-10 rounded-xl bg-slate-100 overflow-clip outline">
        <img src="/images/henooks.png" alt="" class="object-cover" />
      </div>
    </div>
  </div>
</template>
