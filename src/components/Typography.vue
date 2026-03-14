<script setup>
const texts = [
  { label: 'Text 1', class: 'text-sm sm:text-base md:text-lg text-blue-700 font-sans' },
  { label: 'Text 2', class: 'text-sm sm:text-base md:text-lg text-amber-300 font-mono' },
  { label: 'Text 3', class: 'text-sm sm:text-base md:text-lg text-red-600 font-serif' },
  { label: 'Text 4', class: 'text-sm sm:text-base md:text-lg text-gray-500 font-mycustom' },
  { label: 'Text 5', class: 'text-sm sm:text-base md:text-lg text-green-600 italic' },
  { label: 'Text 6', class: 'text-sm sm:text-base md:text-lg text-sky-200 italic font-bold' },
  { label: 'Text 7', class: 'text-sm sm:text-base md:text-lg text-mauve-400 underline' },
  { label: 'Text 8', class: 'text-sm sm:text-base md:text-lg text-red-300 underline decoration-dotted decoration-4' },
  { label: 'Text 9', class: 'text-sm sm:text-base md:text-lg text-cyan-600 line-through' },
  { label: 'Text 10', class: 'text-sm sm:text-base md:text-lg text-purple-500 overline' },
  { label: 'Text 11', class: 'text-sm sm:text-base md:text-lg text-yellow-600 underline decoration-gray-400 hover:decoration-blue-600 hover:text-red-600' },
  { label: 'Text 12', class: 'text-sm sm:text-base md:text-lg text-green-300 uppercase' },
]
</script>

<template>
    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4 p-4">
      <div v-for="(text, index) in texts" :key="index" 
           class="p-4 bg-gray-50 dark:bg-gray-800 rounded-lg shadow">
        <p :class="text.class" class="break-words">{{ text.label }}</p>
      </div>
    </div>
  </template>
