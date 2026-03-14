<script setup>
const cards = [
  { label: 'Сплошной цвет', class: 'bg-blue-600' },
  { label: 'Opacity 60%', class: 'bg-emerald-500/60 border border-emerald-400/50' },
  { label: 'Linear gradient', class: 'bg-gradient-to-r from-amber-400 to-orange-500' },
  { label: 'Linear gradient', class: 'bg-gradient-to-b from-cyan-400 to-blue-600' },
  { label: 'Multi-stop gradient', class: 'bg-gradient-to-r from-violet-500 via-fuchsia-500 to-pink-500' },
  { label: 'Radial gradient', style: 'background: radial-gradient(circle at center, #ec4899 0%, #8b5cf6 50%, #3b82f6 100%);' },
  { label: 'HSLA', style: 'background-color: hsla(300, 70%, 45%, 0.85);' },
]
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4 p-4">
    <div v-for="(card, index) in cards" :key="index"
         class="rounded-lg p-4 md:p-6 min-h-[100px] md:min-h-[120px] flex items-center justify-center text-white font-medium shadow-lg text-sm md:text-base text-center"
         :class="card.class" :style="card.style">
      {{ card.label }}
    </div>
  </div>
</template>