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
  <div class="w-full flex flex-col px-32 pt-16">
    <div class="">
      <h1 class="font-semibold font-montserrat text-3xl text-center mb-5">Berbagai Mitra Untuk Mendukung
        Ekosistem Digital SISTEM
      </h1>
      <p class="font-normal font-inter text-slate-600 text-center text-sm -mt-4 mb-5 ">Cari berbagai macam event
        teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="w-full flex flex-row items-center justify-between gap-6">
      <div v-for="event in events" :key="event.id"
        class="flex flex-col shadow-lg overflow-hidden shadow-slate-400 rounded-lg">
        <div class="w-full">
          <img :src="event.url" :alt="event.title">
        </div>
        <div class="w-full p-5 text-slate-500">
          <div class="card__caption__title">
            <h4 class="font-semibold font-inter text-lg leading-5 line-clamp-1 text-slate-800">{{ event.title }}</h4>
            <p class="font-normal font-inter text-sm mb-5">{{ event.jenisKelas }} {{ event.durasi }}</p>
          </div>
          <div class="flex flex-row gap-3 justify-start items-center mb-4">
            <img :src="event.peminat.url" :alt="event.peminat.peminat">
            <p class="font-inter text-md text-slate-800 font-semibold">{{ event.peminat.peminat }}</p>
          </div>

          <a href="#" class="text-blue-600">Daftar Sekarang →</a>
        </div>
      </div>
    </div>
  </div>
</template>