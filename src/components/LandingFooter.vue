<script setup>
import logo from '@/assets/img/sistem_white.svg';
import instagram from '@/assets/img/instagram_logo.svg';
import phone_logo from '@/assets/img/phone.svg';
import mail_logo from '@/assets/img/mail.svg';

</script>

<template>
  <footer
    class="flex flex-col items-start justify-between w-full gap-8 px-5 py-5 md:gap-0 md:flex-row md:px-32 md:py-16 bg-blue-950">
    <div class="flex flex-col w-full gap-5 md:gap-8 md:w-1/3">
      <img :src="logo" alt="wtf" class="w-1/4 md:w-1/2 fill-white">
      <div class="address">
        <h5 class="text-xl font-semibold leading-relaxed font-inter text-slate-300">Jogja Office</h5>
        <p class="text-base font-normal leading-relaxed font-inter text-slate-400">Jl. Kresna. Gamping kidul,
          Amberketawang, Kec.Gamping, Kabupaten Sleman, DIY 55294</p>
      </div>
      <div class="address">
        <h5 class="text-xl font-semibold leading-relaxed font-inter text-slate-300">Jakarta Office</h5>
        <p class="text-base font-normal leading-relaxed font-inter text-slate-400">Cibis Nine Building Lantai 11 Jl. TB
          Simatupang No.2, Jakarta Selatan</p>
      </div>
    </div>
    <div class="flex justify-between w-full md:px-0 md:justify-around">
      <div class="flex flex-col w-1/3 gap-4 md:gap-7">
        <h5 class="text-xl font-semibold leading-relaxed text-slate-200 font-inter">Bootcamp</h5>
        <ul class="flex flex-col gap-2 md:gap-5 font-inter text-slate-400">
          <li><a href="#">Devops</a></li>
          <li><a href="#">Quality Assurance</a></li>
          <li><a href="#">Full Stack Developer</a></li>
          <li><a href="#">Project Manager</a></li>
        </ul>
      </div>
      <div class="flex flex-col w-1/3 gap-4 md:gap-7">
        <h5 class="text-xl font-semibold leading-relaxed text-slate-200 font-inter">SISTEM</h5>
        <ul class="flex flex-col gap-2 md:gap-5 font-inter text-slate-400">
          <li><a href="#">Tentang Kami</a></li>
          <li><a href="#">Events</a></li>
          <li><a href="#">FAQ</a></li>
        </ul>
      </div>
    </div>
    <div class="flex flex-col w-full gap-4 mg:gap-7 md:w-1/5">
      <h5 class="text-xl font-semibold leading-relaxed text-white font-inter">Ikuti kami</h5>
      <div class="flex items-center justify-center w-8 h-8 p-1 border-2 border-blue-900 rounded-md">
        <img :src="instagram" alt="Instagram Logo" class="size-[80%] fill-white">
      </div>
      <div class="flex gap-3">
        <img :src="phone_logo" alt="lol" class="fill-green-600 stroke-green-600 size-6">
        <a href="#" class="text-sm font-normal font-inter text-slate-400">+62 812 3456 7890</a>
      </div>
      <div class="flex gap-3">
        <img :src="mail_logo" alt="lol" class="fill-green-600 stroke-green-600 size-6">
        <a href="#" class="text-sm font-normal font-inter text-slate-400">dickycandrapermana@student.uns.ac.id</a>
      </div>
    </div>
  </footer>
</template>