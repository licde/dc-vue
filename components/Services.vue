<script setup>
import { Smartphone, MessageSquare, Layout } from 'lucide-vue-next';
import SectionTitle from './SectionTitle.vue';

const services = [
  {
    title: 'APP开发',
    icon: Smartphone,
    desc: ['购物APP', '社交APP', '综合服务APP', '游戏APP', '商城APP'],
  },
  {
    title: '微信小程序',
    icon: MessageSquare,
    desc: ['微官网小程序', '商城小程序', '小游戏小程序', '服务定制小程序', '智慧门店小程序'],
  },
  {
    title: '软件定制开发',
    icon: Layout,
    desc: ['CRM营销平台', '营销费用管理TPM', '经销商管理DMS', '渠道促销服务CPS', '...'],
  },
  {
    title: '网站建设',
    icon: Layout, 
    desc: ['综合门户网站建设', '企业商城建设', '视频网站建设', '商城网站建设', '...'],
  }
];
</script>

<template>
  <section class="py-20 bg-white">
    <div class="container mx-auto px-4 md:px-6">
      <SectionTitle 
        enTitle="OUR SERVICES"
        cnTitle="我们的服务"
        subtitle="多年来我们秉承着为您多想一步的原则，努力打造一站式定制服务平台"
      />

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div v-for="(service, index) in services" :key="index" class="group p-8 rounded-2xl bg-white hover:shadow-2xl hover:-translate-y-2 transition-all duration-300 border border-gray-50 text-center">
          <div class="w-20 h-20 mx-auto mb-6 bg-blue-50 rounded-2xl flex items-center justify-center group-hover:bg-blue-600 transition-colors">
            <component :is="service.icon" class="w-10 h-10 text-blue-600 group-hover:text-white transition-colors" />
          </div>
          <h3 class="text-xl font-bold text-gray-900 mb-4">{{ service.title }}</h3>
          <div class="space-y-2">
            <p v-for="(item, i) in service.desc" :key="i" class="text-sm text-gray-500">{{ item }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>