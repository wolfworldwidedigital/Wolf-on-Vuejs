<template>
  <CommonLoading />
  <Navbar />
  <PagesHeader imageLink="/img/slid/about.jpg">
    <template v-slot:title>
      Our talented team of creatives blends experience with an unwavering passion for excellence.
    </template>
  </PagesHeader>
  <AboutIntro />
  <Services oStyle="4item" />
  <TestimonialsWithVideo />
  <SkillsCircle from="aboutPage" />
  <Team />
  <MinimalArea />
  <Clients theme="dark" />
  <CallToAction />
  <Footer />
</template>

<script setup>
// Page components
import CommonLoading from '@/components/Common/CommonLoading';
import Navbar from '@/components/Common/Navbar';
import PagesHeader from '@/components/Headers/PagesHeader';
import AboutIntro from '@/components/AboutUs/AboutIntro';
import Services from '@/components/Services/Services';
import TestimonialsWithVideo from '@/components/Testimonials/TestimonialsWithVideo';
import SkillsCircle from '@/components/Skills/SkillsCircle';
import Team from '@/components/Team/Team';
import MinimalArea from '@/components/Others/MinimalArea';
import Clients from '@/components/Clients/Clients';
import CallToAction from '@/components/Others/CallToAction';
import Footer from '@/components/Common/Footer';

// Page Metadata (if it's being utilized somewhere in your application)
definePageMeta({
  layout: "dark",
});

// Page Head for SEO
useHead({
  titleTemplate: `Wolf Worldwide - About (Dark)`
});
</script>

<style scoped>
/* Add component-specific styles here if any */
</style>

