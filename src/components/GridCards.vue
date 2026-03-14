<script setup>
const cards = [
  { image: '/src/assets/images/bg1.png', title: 'Заголовок 1', borderColor: 'border-blue-500', textColor: 'text-blue-500' },
  { image: '/src/assets/images/bg1.png', title: 'Заголовок 2', borderColor: 'border-blue-400', textColor: 'text-blue-400' },
  { image: '/src/assets/images/bg1.png', title: 'Заголовок 3', borderColor: 'border-blue-300', textColor: 'text-blue-300' },
  { image: '/src/assets/images/bg1.png', title: 'Заголовок 4', borderColor: 'border-blue-200', textColor: 'text-blue-200' },
  { image: '/src/assets/images/bg2.jpg', title: 'Заголовок 5', borderColor: 'border-red-500', textColor: 'text-red-500' },
  { image: '/src/assets/images/bg2.jpg', title: 'Заголовок 6', borderColor: 'border-red-400', textColor: 'text-red-400' },
  { image: '/src/assets/images/bg2.jpg', title: 'Заголовок 7', borderColor: 'border-red-300', textColor: 'text-red-300' },
  { image: '/src/assets/images/bg2.jpg', title: 'Заголовок 8', borderColor: 'border-red-200', textColor: 'text-red-200' },
  { image: '/src/assets/images/bg3.jpg', title: 'Заголовок 9', borderColor: 'border-purple-500', textColor: 'text-purple-500' },
  { image: '/src/assets/images/bg3.jpg', title: 'Заголовок 10', borderColor: 'border-purple-400', textColor: 'text-purple-400' },
  { image: '/src/assets/images/bg3.jpg', title: 'Заголовок 11', borderColor: 'border-purple-300', textColor: 'text-purple-300' },
  { image: '/src/assets/images/bg3.jpg', title: 'Заголовок 12', borderColor: 'border-purple-200', textColor: 'text-purple-200' },
]
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4 p-4">
    <div v-for="(card, index) in cards" :key="index" 
         class="flex flex-col items-center gap-4 border p-4 rounded-lg hover:shadow-lg transition-shadow"
         :class="card.borderColor">
      <img :src="card.image" :alt="card.title" class="w-full h-32 object-cover rounded">
      <p :class="card.textColor" class="font-bold text-center">{{ card.title }}</p>
    </div>
  </div>
</template>

