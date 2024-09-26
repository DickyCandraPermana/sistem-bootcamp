<script setup>
import brand from '@/assets/img/brand.svg'
</script>

<template>
  <nav class="flex flex-row items-center justify-between w-full px-32 py-5">
    <img :src="brand" alt="">

    <ul class="flex flex-row items-center justify-between font-inter text-slate-800">
      <li class="mr-8 text-blue-600"><a href="#">Home</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Blog</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">About Us</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Contact Us</a></li>
    </ul>

    <button
      class="py-2 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-full font-sen hover:text-blue-700 hover:bg-transparent px-7">
      Contact Us
    </button>
  </nav>
</template>