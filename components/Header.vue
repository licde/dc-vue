<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { Menu, X } from 'lucide-vue-next';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

const navItems = ['首页', '关于我们', '解决方案', '成功案例', '新闻中心'];
</script>

<template>
  <header :class="['fixed top-0 w-full z-50 transition-all duration-300', isScrolled ? 'bg-white shadow-md py-3' : 'bg-transparent py-5']">
    <div class="container mx-auto px-4 md:px-6 flex items-center justify-between">
      <!-- Logo -->
      <div class="flex items-center gap-2">
        <div class="w-10 h-10 bg-blue-600 rounded-lg flex items-center justify-center text-white font-bold text-xl">
          洞
        </div>
        <div>
          <h1 :class="['text-xl font-bold leading-none', isScrolled ? 'text-gray-900' : 'text-white']">洞察科技</h1>
          <p :class="['text-[10px] leading-none', isScrolled ? 'text-gray-500' : 'text-blue-100']">Dongdong Tech</p>
        </div>
      </div>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8">
        <a 
          v-for="(item, index) in navItems" 
          :key="index" 
          href="#" 
          :class="['text-sm font-medium hover:text-blue-500 transition-colors', isScrolled ? 'text-gray-700' : 'text-white/90']"
        >
          {{ item }}
        </a>
      </nav>

      <!-- CTA Buttons -->
      <div class="hidden md:flex items-center gap-4">
        <div class="flex items-center gap-2">
          <span :class="['text-xs', isScrolled ? 'text-gray-500' : 'text-blue-100']">技术咨询: </span>
          <span :class="['font-bold', isScrolled ? 'text-blue-600' : 'text-white']">400-888-666</span>
        </div>
        <button class="bg-blue-600 text-white px-5 py-2 rounded-full text-sm font-medium hover:bg-blue-700 transition-all shadow-lg hover:shadow-xl">
          免费方案
        </button>
      </div>

      <!-- Mobile Toggle -->
      <button 
        class="md:hidden text-gray-500"
        @click="isMobileMenuOpen = !isMobileMenuOpen"
      >
        <component :is="isMobileMenuOpen ? X : Menu" :class="isScrolled ? 'text-gray-900' : 'text-white'" />
      </button>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isMobileMenuOpen" class="absolute top-full left-0 w-full bg-white shadow-lg py-4 px-4 flex flex-col gap-4 md:hidden border-t">
      <a v-for="(item, index) in navItems" :key="index" href="#" class="text-gray-700 font-medium py-2 border-b border-gray-100">{{ item }}</a>
      <button class="bg-blue-600 text-white px-5 py-3 rounded-lg w-full text-sm font-medium">
        获取免费方案
      </button>
    </div>
  </header>
</template>