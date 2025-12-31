<script setup>
import SectionTitle from './SectionTitle.vue';

const cases = [
  {
    title: '电商酒类直供',
    subtitle: 'APP/小程序',
    category: '电商',
    image: 'https://picsum.photos/seed/wine/800/500',
    layout: 'left',
    color: 'from-blue-100 to-indigo-50'
  },
  {
    title: '考试教育类',
    subtitle: 'APP',
    category: '教育',
    image: 'https://picsum.photos/seed/edu/800/500',
    layout: 'right',
    color: 'from-indigo-50 to-blue-100'
  },
  {
    title: '电商拓新营销',
    subtitle: '小程序',
    category: '营销',
    image: 'https://picsum.photos/seed/market/800/500',
    layout: 'left',
    color: 'from-blue-50 to-sky-100'
  },
  {
    title: '民宿预定类',
    subtitle: '小程序',
    category: '旅游',
    image: 'https://picsum.photos/seed/hotel/800/500',
    layout: 'right',
    color: 'from-gray-50 to-gray-100'
  },
  {
    title: '吃喝玩乐融合平台',
    subtitle: '小程序',
    category: '生活',
    image: 'https://picsum.photos/seed/food/800/500',
    layout: 'left',
    color: 'from-orange-50 to-red-50'
  },
  {
    title: '电商团购类',
    subtitle: '小程序',
    category: '团购',
    image: 'https://picsum.photos/seed/group/800/500',
    layout: 'right',
    color: 'from-purple-50 to-pink-50'
  },
];

const bigScreenCase = {
    title: '数字大屏',
    subtitle: '电脑终端/后台',
    category: '数据可视化',
    image: 'https://picsum.photos/seed/screen/1000/600',
    layout: 'center',
    color: 'from-gray-100 to-gray-200'
};
</script>

<template>
  <section class="py-20 bg-white">
    <div class="container mx-auto px-4 md:px-6">
      <SectionTitle 
        enTitle="CASE PRESENTATION"
        cnTitle="部分案例展示"
        subtitle="多年来我们秉承着为您多想一步的原则，努力打造一站式定制服务平台"
      />

      <div class="space-y-16">
        <div v-for="(item, index) in cases" :key="index" :class="['rounded-3xl overflow-hidden bg-gradient-to-br p-8 md:p-12 shadow-sm', item.color]">
           <div :class="['flex flex-col gap-8 items-center', item.layout === 'right' ? 'md:flex-row-reverse' : 'md:flex-row']">
              
              <!-- Text Content -->
              <div class="flex-1 text-center md:text-left">
                 <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2">{{ item.title }}</h3>
                 <h4 class="text-xl md:text-2xl text-gray-600 mb-8">{{ item.subtitle }}</h4>
                 
                 <div class="flex gap-4 justify-center md:justify-start">
                    <button class="bg-blue-600 text-white px-8 py-2 rounded-full font-medium shadow-lg hover:bg-blue-700 transition-colors">
                       立即咨询
                    </button>
                    <button class="bg-transparent border border-blue-600 text-blue-600 px-8 py-2 rounded-full font-medium hover:bg-blue-50 transition-colors">
                       了解案例
                    </button>
                 </div>
              </div>

              <!-- Image/Mockup -->
              <div class="flex-1 w-full flex justify-center">
                 <div class="relative w-full max-w-sm md:max-w-md">
                    <!-- Simulate Phone Frames using CSS -->
                    <div class="flex gap-4 justify-center">
                        <div class="w-[140px] md:w-[180px] bg-white rounded-[2rem] p-2 shadow-2xl transform translate-y-8">
                            <img :src="`${item.image}?1`" alt="App Screen 1" class="w-full h-[280px] object-cover rounded-[1.5rem]" />
                        </div>
                        <div class="w-[140px] md:w-[180px] bg-white rounded-[2rem] p-2 shadow-2xl -translate-y-4 z-10">
                            <img :src="`${item.image}?2`" alt="App Screen 2" class="w-full h-[280px] object-cover rounded-[1.5rem]" />
                        </div>
                    </div>
                 </div>
              </div>

           </div>
        </div>

        <!-- Big Screen Case -->
        <div class="rounded-3xl overflow-hidden bg-gradient-to-b from-gray-100 to-gray-200 p-8 md:p-16 text-center shadow-sm">
           <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2">{{ bigScreenCase.title }}</h3>
           <h4 class="text-xl text-gray-600 mb-10">{{ bigScreenCase.subtitle }}</h4>
           
           <div class="flex gap-4 justify-center mb-12">
              <button class="bg-blue-600 text-white px-8 py-2 rounded-full font-medium shadow-lg hover:bg-blue-700 transition-colors">
                  立即咨询
              </button>
              <button class="bg-transparent border border-blue-600 text-blue-600 px-8 py-2 rounded-full font-medium hover:bg-blue-50 transition-colors">
                  了解案例
              </button>
           </div>

           <div class="relative max-w-4xl mx-auto">
              <div class="bg-gray-800 rounded-t-xl p-2 pb-0 shadow-2xl">
                  <img src="https://picsum.photos/seed/dashboard/1200/600" alt="Dashboard" class="w-full rounded-t-lg" />
              </div>
              <div class="h-4 bg-gray-700 rounded-b-xl mx-4"></div>
              <div class="w-24 h-12 bg-gray-300 mx-auto" style="clip-path: polygon(20% 0%, 80% 0%, 100% 100%, 0% 100%)"></div>
              <div class="w-32 h-2 bg-gray-400 mx-auto rounded-full"></div>
           </div>
        </div>
      </div>
    </div>
  </section>
</template>