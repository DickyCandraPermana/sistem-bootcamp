<script setup>
import { ref } from 'vue'

// figure
import green from '@/assets/img/figure/image (1).png'
import blue from '@/assets/img/figure/image.png'
import yellow from '@/assets/img/figure/image (4).png'
import maroon from '@/assets/img/figure/image (2).png'
import orange from '@/assets/img/figure/image (3).png'

// services icons
import CommentsImage from '@/assets/img/Comments.svg'
import WeekScheduleImage from '@/assets/img/Week Schedule.svg'
import PostImage from '@/assets/img/Post.svg'

import Star from '@/assets/img/Vector 116.svg'

const services = ref([
  { logo: CommentsImage, title: 'Build Community' },
  { logo: WeekScheduleImage, title: 'Share Event' },
  { logo: PostImage, title: 'Get Information' }
])

</script>

<template>
  <header class="flex flex-col-reverse w-full px-5 py-5 md:flex-row md:px-32 md:py-16">
    <!-- Bagian Kiri -->
    <div class="flex flex-col w-full gap-4 md:gap-8 md:w-1/2">
      <h2 class="text-base font-semibold text-yellow-300 uppercase font-inter">career accelerate</h2>
      <h1 class="text-3xl font-semibold leading-normal md:text-4xl font-inter">Meningkatkan Karir Anda di SISTEM
        Bootcamp</h1>
      <p class="text-xs font-normal leading-relaxed md:text-sm font-inter text-slate-800">Pelajari dari ahli Teknik
        Perangkat Lunak
        yang berpengalaman di SEA dan mempercepat karir Anda sebagai Software Engineer.</p>
      <div class="flex flex-col items-start justify-between w-full gap-4 md:gap-0 md:items-center md:flex-row">
        <div class="flex flex-row items-center justify-start w-full md:justify-between md:w-1/3"
          v-for="service in services" :key="service.title">
          <div class="flex items-center justify-center p-2 rounded-lg icon bg-slate-200">
            <img :src="service.logo" :alt="service.title" class="w-[80%]">
          </div>
          <h4 class="px-3 font-semibold leading-5 text-left font-poppins text-md">{{ service.title }}</h4>
        </div>
      </div>
      <button
        class="px-6 py-2 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-full max-w-40 font-sen hover:text-blue-700 hover:bg-transparent">
        Contact Us
      </button>
    </div>
    <!-- Bagian Kiri end -->

    <!-- Bagian Kanan -->
    <div class="flex items-center justify-end w-full mb-10 md:mb-0 md:w-1/2">
      <div class="grid grid-cols-3 grid-rows-3">
        <div class="col-span-1 row-span-3 p-2 overflow-hidden rounded-lg">
          <img :src="green" alt="figure" class="mb-2">
          <img :src="maroon" alt="figure">
        </div>
        <div class="col-span-1 row-span-3 p-2 overflow-hidden rounded-lg">
          <img :src="blue" alt="figure" class="mb-2">
          <img :src="orange" alt="figure">
        </div>
        <div class="col-span-1 row-span-3 p-2 my-auto overflow-hidden rounded-lg">
          <img :src="Star" alt="" class="ml-6">
          <img :src="yellow" alt="figure" class="my-3">
          <img :src="Star" alt="" class="ml-2">
        </div>
      </div>
    </div>
    <!-- Bagian Kanan end -->
  </header>
</template>