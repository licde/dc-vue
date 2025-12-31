<script setup>
import { Lightbulb, TrendingUp, Cpu, Landmark, Handshake, Briefcase, LayoutGrid, Award } from 'lucide-vue-next';
import SectionTitle from './SectionTitle.vue';

const supportItems = [
  { title: '智慧招商', desc: '大数据精准招商，全程招商', icon: Lightbulb, color: 'bg-blue-100' },
  { title: '智慧运营', desc: '智能竞价，多元化社群', icon: TrendingUp, color: 'bg-indigo-100' },
  { title: '智慧物联', desc: '智能停车，智能门禁', icon: Cpu, color: 'bg-cyan-100' },
  { title: '智慧政务', desc: '大数据精准获客，在线申报', icon: Landmark, color: 'bg-sky-100' },
  { title: '产业合作', desc: '大数据精准匹配，上下游供应链', icon: Handshake, color: 'bg-teal-100' },
  { title: '智慧投融', desc: '科技金融体系，投融资平台', icon: Briefcase, color: 'bg-blue-100' },
  { title: '数观园区', desc: '定制数据大屏，数字沙盘', icon: LayoutGrid, color: 'bg-purple-100' },
  { title: '创新创业', desc: '项目推荐，政策扶持', icon: Award, color: 'bg-blue-100' },
];
</script>

<template>
  <section class="py-20 bg-gray-50">
    <div class="container mx-auto px-4 md:px-6">
      <SectionTitle 
        cnTitle="全方位功能支持"
      />

      <div class="grid grid-cols-2 md:grid-cols-4 gap-x-6 gap-y-12">
        <div v-for="(item, index) in supportItems" :key="index" class="flex flex-col items-center text-center">
          <div :class="['w-20 h-20 rounded-full flex items-center justify-center mb-6 shadow-sm hover:scale-110 transition-transform cursor-pointer', item.color]">
            <component :is="item.icon" class="w-8 h-8 text-blue-700" />
          </div>
          <h4 class="text-lg font-bold text-gray-800 mb-2">{{ item.title }}</h4>
          <p class="text-xs text-gray-500 max-w-[150px] leading-relaxed">{{ item.desc }}</p>
        </div>
      </div>

      <!-- Access Points Bar -->
      <div class="mt-20">
        <p class="text-gray-600 font-medium mb-6">提供多端用户入口</p>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
          <button class="flex items-center justify-center gap-3 bg-cyan-400 text-white py-4 rounded-lg hover:opacity-90 transition-opacity">
             <span class="text-2xl">📱</span> 移动端APP
          </button>
          <button class="flex items-center justify-center gap-3 bg-emerald-400 text-white py-4 rounded-lg hover:opacity-90 transition-opacity">
             <span class="text-2xl">💬</span> 微信服务号/小程序
          </button>
          <button class="flex items-center justify-center gap-3 bg-blue-500 text-white py-4 rounded-lg hover:opacity-90 transition-opacity">
             <span class="text-2xl">💻</span> WEB网站
          </button>
          <button class="flex items-center justify-center gap-3 bg-slate-500 text-white py-4 rounded-lg hover:opacity-90 transition-opacity">
             <span class="text-2xl">📺</span> 智能终端
          </button>
        </div>
      </div>
    </div>
  </section>
</template>