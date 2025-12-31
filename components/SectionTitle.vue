<script setup>
defineProps({
  enTitle: String,
  cnTitle: String,
  subtitle: String,
  light: Boolean
});
</script>

<template>
  <div class="text-center mb-12">
    <h3 v-if="enTitle" :class="['text-sm tracking-widest uppercase font-semibold mb-2', light ? 'text-blue-100' : 'text-blue-500 opacity-60']">
      {{ enTitle }}
    </h3>
    <h2 :class="['text-3xl font-bold mb-4', light ? 'text-white' : 'text-gray-900']">
      {{ cnTitle }}
    </h2>
    <div v-if="subtitle" :class="['w-12 h-1 mx-auto mb-4', light ? 'bg-white' : 'bg-blue-600']"></div>
    <p v-if="subtitle" :class="['text-sm', light ? 'text-gray-200' : 'text-gray-500']">
      {{ subtitle }}
    </p>
  </div>
</template>