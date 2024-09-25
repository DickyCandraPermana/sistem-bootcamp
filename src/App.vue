<script setup>
import Navbar from '@/components/MainNavbar.vue'
import MainHeader from '@/components/LandingPageHeader.vue'
import ContentKerjasama from '@/components/ContentKerjasama.vue'
import LandingBlog from '@/components/LandingBlog.vue'
import LandingAbout from '@/components/LandingAbout.vue'

</script>

<template>
  <Navbar />
  <MainHeader />
  <main>
    <ContentKerjasama />
    <LandingBlog />
    <LandingAbout />
  </main>
</template>
