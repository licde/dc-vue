<script setup>
import { ArrowRight, BarChart3, Database, ShieldCheck } from 'lucide-vue-next';
</script>

<template>
  <section class="relative w-full overflow-hidden">
    <!-- Background with Gradient -->
    <div class="absolute inset-0 bg-gradient-to-br from-blue-900 via-blue-700 to-indigo-800 z-0">
       <!-- Decorative Circles -->
       <div class="absolute top-[-20%] right-[-10%] w-[800px] h-[800px] bg-blue-500/20 rounded-full blur-3xl"></div>
       <div class="absolute bottom-[-10%] left-[-10%] w-[600px] h-[600px] bg-indigo-500/20 rounded-full blur-3xl"></div>
    </div>

    <div class="container mx-auto px-4 md:px-6 relative z-10 pt-32 pb-20 md:pt-48 md:pb-32">
      <div class="flex flex-col md:flex-row items-center justify-between gap-12">
        
        <!-- Left Content -->
        <div class="flex-1 text-center md:text-left text-white">
          <h2 class="text-xl md:text-2xl font-light mb-4 tracking-wide text-blue-200">助力企业数字化升级</h2>
          <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
            探索无限可能<br />
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-200 to-white">
              企业智能化转型行业
            </span>
          </h1>
          <p class="text-blue-100/80 mb-8 max-w-lg mx-auto md:mx-0">
            您身边的解决方案专家。提供全方位的技术支持与创新服务，驱动业务增长。
            THE SOLUTION EXPERTS AROUND YOU
          </p>
          
          <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
             <button class="bg-white text-blue-700 px-8 py-3 rounded-full font-bold hover:bg-blue-50 transition-all flex items-center justify-center gap-2 shadow-lg">
                立即咨询 <ArrowRight :size="18" />
             </button>
             <button class="border border-blue-300 text-blue-100 px-8 py-3 rounded-full font-medium hover:bg-white/10 transition-all">
                查看案例
             </button>
          </div>
        </div>

        <!-- Right Visual (Abstract 3D Representation) -->
        <div class="flex-1 w-full max-w-[600px] relative hidden md:block">
          <div class="relative w-full aspect-[4/3]">
            <!-- Isometric Platform Simulation -->
            <div class="absolute inset-x-0 bottom-0 h-1/2 bg-white/5 rounded-2xl transform rotate-x-60 scale-y-50 border border-white/10 backdrop-blur-sm"></div>
            
            <!-- Floating Elements -->
            <div class="absolute top-10 left-10 bg-gradient-to-br from-blue-400 to-blue-600 p-4 rounded-xl shadow-2xl transform -rotate-6 border border-white/20 animate-pulse">
              <BarChart3 class="text-white w-12 h-12" />
            </div>
            
            <div class="absolute top-0 right-20 bg-gradient-to-br from-indigo-400 to-indigo-600 p-6 rounded-2xl shadow-2xl transform rotate-12 border border-white/20">
              <Database class="text-white w-16 h-16" />
              <div class="mt-2 h-2 w-16 bg-white/30 rounded-full"></div>
              <div class="mt-2 h-2 w-10 bg-white/30 rounded-full"></div>
            </div>
            
            <div class="absolute bottom-20 left-1/3 bg-white p-4 rounded-xl shadow-xl z-10 flex items-center gap-3">
               <div class="bg-green-100 p-2 rounded-lg">
                  <ShieldCheck class="text-green-600 w-6 h-6" />
               </div>
               <div>
                  <div class="text-gray-900 font-bold">100% 安全</div>
                  <div class="text-xs text-gray-500">企业级防护</div>
               </div>
            </div>
            
            <!-- Chart Line -->
            <svg class="absolute top-1/4 left-0 w-full h-full pointer-events-none" viewBox="0 0 400 200">
              <path d="M 50 150 C 100 150, 150 100, 200 80 S 300 50, 350 20" fill="none" stroke="url(#lineGradient)" stroke-width="4" stroke-linecap="round" />
              <defs>
                <linearGradient id="lineGradient" x1="0" y1="0" x2="1" y2="0">
                  <stop offset="0%" stop-color="#60A5FA" stop-opacity="0" />
                  <stop offset="50%" stop-color="#F472B6" />
                  <stop offset="100%" stop-color="#F87171" />
                </linearGradient>
              </defs>
            </svg>
          </div>
        </div>
      </div>
    </div>

    <!-- Stats Bar -->
    <div class="bg-gray-900 text-white py-6 border-t border-gray-800">
      <div class="container mx-auto px-4 md:px-6 flex flex-wrap justify-center md:justify-around gap-8 text-center">
         <div class="flex items-center gap-3">
           <span class="text-3xl md:text-4xl font-bold text-blue-500">10<span class="text-lg align-top">+</span></span>
           <div class="text-left text-xs text-gray-400">
              <div>年行业经验</div>
              <div>10年行业运营管理团队</div>
           </div>
         </div>
         <div class="w-px h-10 bg-gray-700 hidden md:block"></div>
         <div class="flex items-center gap-3">
           <span class="text-3xl md:text-4xl font-bold text-blue-500">100<span class="text-lg align-top">+</span></span>
           <div class="text-left text-xs text-gray-400">
              <div>客户</div>
              <div>服务客户超过100家</div>
           </div>
         </div>
         <div class="w-px h-10 bg-gray-700 hidden md:block"></div>
         <div class="flex items-center gap-3">
           <span class="text-3xl md:text-4xl font-bold text-blue-500">6<span class="text-lg align-top">+</span></span>
           <div class="text-left text-xs text-gray-400">
              <div>大特色服务</div>
              <div>放心、贴心、用心、热心、专心、安心</div>
           </div>
         </div>
      </div>
    </div>
  </section>
</template>