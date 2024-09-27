<script setup>
import { ref } from 'vue'

import img1 from '@/assets/img/cerita/img-1.png';
import img2 from '@/assets/img/cerita/img-2.png';
import img3 from '@/assets/img/cerita/img-3.png';

const stories = ref([
  {
    id: 0,
    img: img1,
    name: "Syhabudin Ahmad",
    job: "Project Manager Solutionlabs",
    story: "Program SISTEM top markotop. Selama belajar cara penyampaian dan arahan mentor unik selain itu mentor juga siap membantu kami jika ada kesulitan."
  },
  {
    id: 1,
    img: img2,
    name: "Annastasya KW",
    job: "Project Manager Solutionlabs",
    story: "Dulu sebelum belajar tentang PM di SISTEM sering kesulitan buat manage project. Setelah ikut bootcamp SISTEM jadi tau gimana biar project itu bisa selesai dan achive."
  },
  {
    id: 2,
    img: img3,
    name: "Tasya WA",
    job: "Quality Assurance Solutions",
    story: "Kemarin waktu belajar coding di sini enak banget. Kita di kelas bener-bener dibimbing dari nol (0) sama mentor dari pembelajarannya juga gampang dipahami."
  }
])
</script>

<template>
  <div class="flex flex-col w-full px-5 py-5 md:px-32 md:py-16">
    <div class="flex flex-col w-full">
      <h1 class="text-3xl font-semibold text-center mb-7 font-montserrat">Cerita Sukses Peserta</h1>
      <p class="mb-5 -mt-4 text-xs font-normal text-center md:text-sm font-inter text-slate-500">Cari berbagai macam
        event
        teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="flex flex-col items-center justify-between w-full gap-5 mt-5 md:flex-row">
      <div v-for="story in stories" :key="story.id"
        class="p-8 pb-10 transition-all duration-500 bg-white rounded-md shadow-md group hover:-translate-y-3 shadow-slate-400">
        <div class="flex flex-row items-center justify-start gap-3 mb-8">
          <img :src="story.img" :alt="story.name" class="transition-all duration-500 size-16 group-hover:scale-125">
          <div class="flex flex-col gap-1">
            <h3 class="text-lg font-semibold">{{ story.name }}</h3>
            <p class="text-xs font-normal text-slate-500 font-inter">{{ story.job }}</p>
          </div>
        </div>
        <p class="text-sm font-normal leading-relaxed text-slate-800 font-inter">{{ story.story }}</p>
      </div>
    </div>
  </div>
</template>