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
  <header class="w-full flex px-32 py-16">
    <!-- Bagian Kiri -->
    <div class="w-1/2 flex flex-col gap-8">
      <h2 class="uppercase font-inter text-yellow-300 font-semibold text-md">career accelerate</h2>
      <h1 class="font-semibold font-inter text-4xl leading-relaxed">Meningkatkan Karir Anda di SISTEM Bootcamp</h1>
      <p class="font-normal font-inter text-slate-800 text-sm leading-relaxed">Pelajari dari ahli Teknik Perangkat Lunak
        yang
        berpengalaman di SEA
        dan
        mempercepat karir Anda sebagai
        Software Engineer.</p>
      <div class="flex flex-row w-full items-center justify-between">
        <div class="flex flex-row items-center justify-between" v-for="service in services" :key="service">
          <div class="icon bg-slate-200 rounded-lg p-2">
            <img :src="service.logo" :alt="service.title">
          </div>
          <h4 class="font-semibold px-3 font-poppins text-md leading-5">{{ service.title }}</h4>
        </div>
      </div>
      <button
        class="text-white max-w-40 font-sen bg-blue-700 rounded-full border border-blue-700 font-bold hover:text-blue-700 hover:bg-transparent transition-all duration-500 py-2 px-6">
        Contact Us
      </button>
    </div>
    <!-- Bagian Kiri end -->

    <!-- Bagian Kanan -->
    <div class="w-1/2 flex justify-end items-center">
      <div class="grid grid-cols-3 grid-rows-3">
        <div class="col-span-1 row-span-3 rounded-lg overflow-hidden p-2">
          <img :src="green" alt="figure" class="mb-2">
          <img :src="maroon" alt="figure">
        </div>
        <div class="col-span-1 row-span-3 rounded-lg overflow-hidden p-2">
          <img :src="blue" alt="figure" class="mb-2">
          <img :src="orange" alt="figure">
        </div>
        <div class="col-span-1 row-span-3 rounded-lg overflow-hidden p-2 my-auto">
          <img :src="Star" alt="">
          <img :src="yellow" alt="figure" class="my-3">
          <img :src="Star" alt="">
        </div>
      </div>
    </div>
    <!-- Bagian Kanan end -->
  </header>
</template>