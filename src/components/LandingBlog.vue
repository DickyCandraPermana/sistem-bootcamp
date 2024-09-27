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
  <div class="flex flex-col w-full px-5 py-5 mt-5 md:px-32 md:pt-16">
    <div class="">
      <h1 class="text-xl font-semibold text-center md:text-3xl mb-7 font-montserrat">Pilih Pengalaman Event Terbaik
      </h1>
      <p class="mb-5 -mt-4 text-xs font-normal text-center md:text-sm font-inter text-slate-500 ">Cari berbagai macam
        event teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="grid items-center justify-between w-full grid-cols-2 gap-4 md:gap-6 md:flex md:flex-row">
      <div v-for="event in events" :key="event.id"
        class="flex flex-col overflow-hidden transition-all duration-500 rounded-lg shadow-lg shadow-slate-400 hover:-translate-y-3 group">
        <div class="w-full">
          <img :src="event.url" :alt="event.title"
            class="object-cover overflow-hidden transition-all duration-500 group-hover:scale-110">
        </div>
        <div class="w-full p-5 text-slate-500">
          <div class="">
            <h4
              class="text-base font-semibold leading-5 md:text-lg font-inter line-clamp-2 md:line-clamp-1 text-slate-800">
              {{
                event.title
              }}</h4>
            <p class="mb-5 text-xs font-normal md:text-sm font-inter">{{ event.jenisKelas }} {{ event.durasi }}</p>
          </div>
          <div class="flex flex-row items-center justify-start gap-2 mb-4 md:gap-3">
            <img :src="event.peminat.url" :alt="event.peminat.peminat" class="w-1/2 md:w-14">
            <p class="text-xs font-semibold md:text-sm font-inter md:text-md text-slate-800">{{ event.peminat.peminat }}
            </p>
          </div>

          <a href="#" class="text-xs text-blue-600 md:text-md">Daftar Sekarang →</a>
        </div>
      </div>
    </div>
  </div>
</template>