<script setup lang="ts">

import { 
  Navbar,
  Hero,
  About,
  Destinations,
  Download,
  Testimonials,
  Footer
} from "./components";
import TrendingStories from "./components/home/TrendingStories.vue";

</script>

<template>
  <main class="main-page-container">
     <Navbar/>
     <Hero/>
     <About/>
     <Destinations/>
     <Download/>
     <Testimonials/>
     <TrendingStories/>
     <Footer/>
  </main>
</template>


