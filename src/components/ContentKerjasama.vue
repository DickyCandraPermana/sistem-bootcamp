<script setup>
import { ref } from "vue";

import img1 from "@/assets/img/partner/img-1.png";
import img2 from "@/assets/img/partner/img-2.png";
import img3 from "@/assets/img/partner/img-3.png";
import img4 from "@/assets/img/partner/img-4.png";
import img5 from "@/assets/img/partner/img-5.png";
import img6 from "@/assets/img/partner/img-6.png";

const partners = ref([
  { id: 0, url: img1 },
  { id: 1, url: img2 },
  { id: 2, url: img3 },
  { id: 3, url: img4 },
  { id: 4, url: img5 },
  { id: 5, url: img6 },
]);
</script>

<template>
  <div class="flex flex-col items-center justify-between w-full px-5 py-5 md:px-32 md:py-16">
    <h1 class="mb-5 text-xl font-semibold text-center md:leading-relaxed font-montserrat md:text-3xl">
      Berbagai Mitra Untuk Mendukung Ekosistem Digital SISTEM
    </h1>
    <div class="flex flex-row items-center justify-between w-full overflow-visible">
      <div class="block p-4" v-for="partner in partners" :key="partner.id">
        <img :src="partner.url" alt="Partner Logo" />
      </div>
    </div>
  </div>
</template>
