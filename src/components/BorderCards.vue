<script setup>
const cards = [
  { label: 'border (1px)', class: 'border border-gray-400 bg-gray-50 dark:bg-gray-800 dark:text-white' },
  { label: 'border-4', class: 'border-4 border-gray-600 bg-gray-50 dark:bg-gray-800 dark:text-white' },
  { label: 'border-blue-500', class: 'border-2 border-blue-500 bg-blue-50 dark:bg-blue-900 dark:text-white text-blue-800 dark:text-blue-200' },
  { label: 'rounded-lg', class: 'border-2 border-emerald-500 rounded-lg bg-emerald-50 dark:bg-emerald-900 dark:text-white text-emerald-800 dark:text-emerald-200' },
  { label: 'rounded-3xl', class: 'border-2 border-violet-500 rounded-3xl bg-violet-50 dark:bg-violet-900 dark:text-white text-violet-800 dark:text-violet-200' },
  { label: 'border-dashed', class: 'border-2 border-dashed border-amber-500 bg-amber-50 dark:bg-amber-900 dark:text-white text-amber-800 dark:text-amber-200' },
  { label: 'border-dotted', class: 'border-2 border-dotted border-rose-500 bg-rose-50 dark:bg-rose-900 dark:text-white text-rose-800 dark:text-rose-200' },
  { label: 'border-double', class: 'border-4 border-double border-indigo-600 bg-indigo-50 dark:bg-indigo-900 dark:text-white text-indigo-800 dark:text-indigo-200' },
  { label: 'different-sides', class: 'border-l-4 border-t-2 border-r border-b border-l-orange-500 border-t-amber-400 border-r-gray-300 border-b-gray-300 bg-orange-50 dark:bg-orange-900 dark:text-white text-orange-800 dark:text-orange-200' },
]
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 p-4">
    <div v-for="(card, index) in cards" :key="index"
         class="p-4 md:p-6 min-h-[80px] md:min-h-[100px] flex items-center justify-center font-medium text-center text-sm md:text-base"
         :class="card.class">
      {{ card.label }}
    </div>
  </div>
</template>