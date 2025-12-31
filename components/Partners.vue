<script setup>
import SectionTitle from './SectionTitle.vue';
</script>

<template>
  <section class="py-20 bg-gray-50">
     <div class="container mx-auto px-4 text-center">
        <SectionTitle cnTitle="合作伙伴" subtitle="携手各行精英，共创财富，合作共赢" />
        
        <div class="grid grid-cols-2 md:grid-cols-6 gap-8 items-center opacity-70 grayscale hover:grayscale-0 transition-all duration-500">
           <!-- Simulating Logos with Text/Placeholders -->
           <div class="flex flex-col items-center gap-2">
              <div class="text-red-600 font-bold text-xl border border-red-600 rounded-full w-12 h-12 flex items-center justify-center">五</div>
              <span class="text-sm font-bold">五粮液集团</span>
           </div>
           <div class="flex flex-col items-center gap-2">
              <div class="text-gray-800 font-serif font-bold text-xl italic">ShuiJingFang</div>
              <span class="text-sm font-bold">水井坊</span>
           </div>
           <div class="flex flex-col items-center gap-2">
              <div class="text-yellow-600 font-bold text-xl">🐴</div>
              <span class="text-sm font-bold">法国赛马</span>
           </div>
           <div class="flex flex-col items-center gap-2">
              <div class="text-blue-600 font-bold text-2xl">1919</div>
              <span class="text-sm font-bold">1919</span>
           </div>
            <div class="flex flex-col items-center gap-2">
              <div class="text-blue-900 font-bold text-xl rounded-full border-2 border-blue-900 w-12 h-12 flex items-center justify-center">科</div>
              <span class="text-sm font-bold">科伦</span>
           </div>
           <div class="flex flex-col items-center gap-2">
              <div class="text-red-600 font-bold text-xl">❄️</div>
              <span class="text-sm font-bold">中国石油</span>
           </div>
        </div>
     </div>
  </section>
</template>