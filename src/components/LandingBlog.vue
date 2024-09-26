<script setup>
import { ref } from "vue";

import img1 from "@/assets/img/blog/img1.png";
import img2 from "@/assets/img/blog/img2.png";
import img3 from "@/assets/img/blog/img3.png";
import img4 from "@/assets/img/blog/img4.png";
import profile from "@/assets/img/blog/profile_pict.png";

const events = ref([
  {
    id: 0,
    url: img1,
    title: "Quality Assurance",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 1,
    url: img2,
    title: "Project Manager",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 2,
    url: img3,
    title: "Development Operational",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 3,
    url: img4,
    title: "Fullstack Developer",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  }
])

</script>

<template>
  <div class="flex flex-col w-full px-32 pt-16 mt-5">
    <div class="">
      <h1 class="text-3xl font-semibold text-center mb-7 font-montserrat">Berbagai Mitra Untuk Mendukung
        Ekosistem Digital SISTEM
      </h1>
      <p class="mb-5 -mt-4 text-sm font-normal text-center font-inter text-slate-500 ">Cari berbagai macam event
        teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="flex flex-row items-center justify-between w-full gap-6">
      <div v-for="event in events" :key="event.id"
        class="flex flex-col overflow-hidden rounded-lg shadow-lg shadow-slate-400">
        <div class="w-full">
          <img :src="event.url" :alt="event.title">
        </div>
        <div class="w-full p-5 text-slate-500">
          <div class="">
            <h4 class="text-lg font-semibold leading-5 font-inter line-clamp-1 text-slate-800">{{ event.title }}</h4>
            <p class="mb-5 text-sm font-normal font-inter">{{ event.jenisKelas }} {{ event.durasi }}</p>
          </div>
          <div class="flex flex-row items-center justify-start gap-3 mb-4">
            <img :src="event.peminat.url" :alt="event.peminat.peminat">
            <p class="font-semibold font-inter text-md text-slate-800">{{ event.peminat.peminat }}</p>
          </div>

          <a href="#" class="text-blue-600">Daftar Sekarang →</a>
        </div>
      </div>
    </div>
  </div>
</template>