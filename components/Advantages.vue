<script setup>
import { Award, Users, ShieldCheck, ThumbsUp, Database, Headphones, Search, PenTool, FileText, Code, CheckSquare, Rocket } from 'lucide-vue-next';
import SectionTitle from './SectionTitle.vue';

const advantages = [
  { title: '专业性强', desc: '核心团队数十年专业从事互联网定制开发', icon: Award },
  { title: '实战经验丰富', desc: '多年来我们服务了数百家企业', icon: Users },
  { title: '专业化服务流程', desc: '从沟通到签约到项目完成，严格把控', icon: ShieldCheck },
  { title: '品牌口碑好', desc: '四川省优秀创新型企业', icon: ThumbsUp },
  { title: '渠道资源丰富', desc: '积累多年，切实可行的定制开发', icon: Database },
  { title: '售后体系完善', desc: '专业团队7*12小时服务售后无忧', icon: Headphones },
];

const processSteps = [
  { step: '01', title: '需求调研', desc: 'Investigate', icon: Search },
  { step: '02', title: '签订合同', desc: 'Contract', icon: PenTool },
  { step: '03', title: '项目评估', desc: 'Assessment', icon: FileText },
  { step: '04', title: '项目开发', desc: 'Development', icon: Code },
  { step: '05', title: '项目验收', desc: 'Acceptance', icon: CheckSquare },
  { step: '06', title: '全面上线', desc: 'Launch', icon: Rocket },
];

const getIconClass = (index) => {
  if (index % 3 === 0) return 'bg-blue-100 text-blue-600';
  if (index % 3 === 1) return 'bg-cyan-100 text-cyan-600';
  return 'bg-indigo-100 text-indigo-600';
};
</script>

<template>
  <section class="py-20 bg-white">
    <div class="container mx-auto px-4 md:px-6">
      <SectionTitle 
        enTitle="SERVICE ADVANTAGES"
        cnTitle="服务优势"
        subtitle="多年来我们秉承着为您多想一步的原则，努力打造一站式定制服务平台"
      />

      <!-- Advantages Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 mb-20">
        <div v-for="(adv, index) in advantages" :key="index" class="flex flex-col items-center text-center p-6 bg-slate-50/50 rounded-xl hover:bg-white hover:shadow-lg transition-all">
          <div :class="['w-16 h-16 rounded-full flex items-center justify-center mb-4', getIconClass(index)]">
            <component :is="adv.icon" class="w-8 h-8" />
          </div>
          <h4 class="text-lg font-bold text-gray-900 mb-2">{{ adv.title }}</h4>
          <p class="text-sm text-gray-500">{{ adv.desc }}</p>
        </div>
      </div>

      <!-- Delivery Process -->
      <div class="text-center mb-12">
         <h3 class="text-2xl font-bold mb-2">最快7天云效交付</h3>
         <p class="text-gray-400 text-sm">洞察科技标准服务流程</p>
      </div>

      <div class="relative">
        <!-- Connector Line (Desktop) -->
        <div class="hidden md:block absolute top-10 left-0 w-full h-0.5 bg-blue-100 -z-10"></div>
        
        <div class="grid grid-cols-2 md:grid-cols-6 gap-6">
           <div v-for="(step, index) in processSteps" :key="index" class="bg-white pt-4 pb-6 flex flex-col items-center">
              <div class="bg-white p-2">
                <component :is="step.icon" class="w-8 h-8 text-blue-500 mb-2" />
              </div>
              <div class="text-2xl font-bold text-gray-900 mb-1">{{ step.step }}</div>
              <div class="text-sm font-medium text-gray-700">{{ step.title }}</div>
              <div class="text-xs text-gray-400 mt-1">{{ step.desc }}</div>
           </div>
        </div>
      </div>

    </div>
  </section>
</template>