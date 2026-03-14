<script setup>
const cards = [
  { label: 'w-50', class: 'bg-gradient-to-b from-red-700 w-[50px] h-[50px]' },
  { label: 'h-50', class: 'bg-gradient-to-b from-emerald-500/60 border border-emerald-400/50 w-[50px] h-[50px]' },
  { label: '50x50', class: 'bg-gradient-to-r from-amber-400 to-orange-500 w-[50px] h-[50px]' },
  { label: '80x80', class: 'bg-gradient-to-b from-cyan-400 to-blue-600 w-[80px] h-[80px]' },
  { label: 'h-190', class: 'bg-gradient-to-r from-orange-500 via-yellow-500 to-red-500 w-[100px] h-[190px]' },
  { label: '180x180', style: 'background: radial-gradient(circle at center, #00FFF7 0%, #00FF7B 50%, #00FF19 100%); width: 180px; height: 180px;' },
]
</script>

<template>
    <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 p-4">
      <div v-for="(card, index) in cards" :key="index"
           class="rounded-lg shadow-lg flex items-center justify-center text-black font-bold"
           :class="card.class" :style="card.style">
        {{ card.label }}
      </div>
    </div>
  </template>
