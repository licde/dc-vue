<script setup>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Services from './components/Services.vue';
import Support from './components/Support.vue';
import Advantages from './components/Advantages.vue';
import Cases from './components/Cases.vue';
import Partners from './components/Partners.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div class="min-h-screen bg-white font-sans text-gray-900 selection:bg-blue-100 selection:text-blue-900">
    <Header />
    <main>
      <Hero />
      <Services />
      <Support />
      <Advantages />
      <Cases />
      <Partners />
    </main>
    <Footer />
  </div>
</template>