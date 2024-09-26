<script setup>
import Navbar from '@/components/MainNavbar.vue'
import MainHeader from '@/components/LandingPageHeader.vue'
import ContentKerjasama from '@/components/ContentKerjasama.vue'
import LandingBlog from '@/components/LandingBlog.vue'
import LandingAbout from '@/components/LandingAbout.vue'
import LandingCeritaSukses from '@/components/LandingCeritaSukses.vue'
import LandingJoinus from './components/LandingJoinus.vue'
import LandingFooter from './components/LandingFooter.vue'

</script>

<template>
  <Navbar />
  <MainHeader />
  <main>
    <ContentKerjasama />
    <LandingBlog />
    <LandingAbout />
    <LandingCeritaSukses />
    <LandingJoinus />
  </main>
  <LandingFooter />
</template>
