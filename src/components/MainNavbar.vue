<script setup>
import brand from '@/assets/img/brand.svg'
</script>

<template>
  <nav class="flex flex-row w-full justify-between items-center px-32 py-5">
    <img :src="brand" alt="">

    <ul class="flex font-inter flex-row justify-between items-center text-slate-800">
      <li class="mr-8 hover:text-slate-600"><a href="#">Blog</a></li>
      <li class="mr-8 hover:text-slate-600"><a href="#">Home</a></li>
      <li class="mr-8 hover:text-slate-600"><a href="#">About Us</a></li>
      <li class="mr-8 hover:text-slate-600"><a href="#">Contact Us</a></li>
    </ul>

    <button
      class="text-white font-sen bg-blue-700 rounded-full border border-blue-700 font-bold hover:text-blue-700 hover:bg-transparent transition-all duration-500 py-2 px-7">
      Contact Us
    </button>
  </nav>
</template>