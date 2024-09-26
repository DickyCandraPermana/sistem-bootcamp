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
  <header class="flex w-full px-32 py-16">
    <!-- Bagian Kiri -->
    <div class="flex flex-col w-1/2 gap-8">
      <h2 class="text-base font-semibold text-yellow-300 uppercase font-inter">career accelerate</h2>
      <h1 class="text-4xl font-semibold leading-normal font-inter">Meningkatkan Karir Anda di SISTEM Bootcamp</h1>
      <p class="text-sm font-normal leading-relaxed font-inter text-slate-800">Pelajari dari ahli Teknik Perangkat Lunak
        yang berpengalaman di SEA dan mempercepat karir Anda sebagai Software Engineer.</p>
      <div class="flex flex-row items-center justify-between w-full">
        <div class="flex flex-row items-center justify-between" v-for="service in services" :key="service">
          <div class="p-2 rounded-lg icon bg-slate-200">
            <img :src="service.logo" :alt="service.title">
          </div>
          <h4 class="px-3 font-semibold leading-5 font-poppins text-md">{{ service.title }}</h4>
        </div>
      </div>
      <button
        class="px-6 py-2 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-full max-w-40 font-sen hover:text-blue-700 hover:bg-transparent">
        Contact Us
      </button>
    </div>
    <!-- Bagian Kiri end -->

    <!-- Bagian Kanan -->
    <div class="flex items-center justify-end w-1/2">
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
          <img :src="Star" alt="">
          <img :src="yellow" alt="figure" class="my-3">
          <img :src="Star" alt="">
        </div>
      </div>
    </div>
    <!-- Bagian Kanan end -->
  </header>
</template>