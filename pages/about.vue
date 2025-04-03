<script setup>
const timelineItems = [
  {
    title: "Company Founded",
    description:
      "Our journey began with a vision to transform the industry through innovative solutions and cutting-edge technology.",
    date: "October 2024",
    image: "/images/ceo.png",
  },
  {
    title: "Looking For First Major Client",
    description:
      "Looking forward to secure our first enterprise partnership, validating our approach and opening doors to new opportunities.",
    date: "Current",
    image: "/images/truck.png",
  },
  // {
  //   title: "International Expansion",
  //   description:
  //     "Established our global presence with new offices in London, Tokyo, and Singapore to better serve our international clients.",
  //   date: "June 2021",
  //   image: "/images/coffee-beans.png",
  // },
  // {
  //   title: "Product Launch",
  //   description:
  //     "Unveiled our flagship platform after months of development, receiving overwhelming positive feedback from the market.",
  //   date: "September 2022",
  //   image: "/images/coffee-beans.png",
  // },
  // {
  //   title: "Industry Recognition",
  //   description:
  //     "Honored with the prestigious Innovation Award, recognizing our commitment to excellence and forward-thinking solutions.",
  //   date: "December 2023",
  //   image: "/images/coffee-beans.png",
  // },
];
</script>
<template>
  <div class="space-y-40">
    <AboutHistory />
    <Mission :about="true" />
    <AboutCoreValues />
    <Processes :timelineItems title="Our Story" />
    <AboutSisters />
    <AboutFaq />
  </div>
</template>
