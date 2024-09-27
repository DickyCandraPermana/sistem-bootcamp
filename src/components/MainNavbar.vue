<script setup>
import { ref } from "vue";

import brand from '@/assets/img/brand.svg'

let isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
}
</script>

<template>
  <nav class="flex flex-row items-center justify-between w-full px-5 py-3 md:px-32 md:py-5">
    <img :src="brand" alt="">

    <ul class="flex-row items-center justify-between hidden text-base md:flex font-inter text-slate-800">
      <li class="mr-8 text-blue-600"><a href="#">Home</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Blog</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">About Us</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Contact Us</a></li>
    </ul>

    <button
      class="hidden py-2 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-full md:block font-sen hover:text-blue-700 hover:bg-transparent px-7">
      Contact Us
    </button>
    <button @click="toggleMenu" class="flex flex-col gap-1 py-2 font-bold text-white md:hidden font-sen">
      <div :class="['h-[2px]', 'w-[20px]', 'bg-black', 'transition-all', 'duration-500', { 'rotate-45': isOpen }]">
      </div>
      <div :class="['h-[2px]', 'w-[20px]', 'bg-black', 'transition-all', 'duration-500', { 'hidden': isOpen }]"></div>
      <div
        :class="['h-[2px]', 'w-[20px]', 'bg-black', 'transition-all', 'duration-500', { '-rotate-45': isOpen, '-translate-y-2': isOpen }]">
      </div>
    </button>
  </nav>
  <div v-if="isOpen" class="absolute z-10 w-full bg-slate-700">
    <ul>
      <li
        class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter hover:bg-slate-300 hover:text-slate-700">
        <a href="">Home</a>
      </li>
      <li
        class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter hover:bg-slate-300 hover:text-slate-700">
        <a href="">Blog</a>
      </li>
      <li
        class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter hover:bg-slate-300 hover:text-slate-700">
        <a href="">About</a>
      </li>
      <li
        class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter hover:bg-slate-300 hover:text-slate-700">
        <a href="">Contact Us</a>
      </li>
    </ul>
  </div>
  <div v-if="isOpen" class="absolute opacity-50 w-svw h-[100vh] transition-all duration-500 bg-slate-800"></div>
</template>