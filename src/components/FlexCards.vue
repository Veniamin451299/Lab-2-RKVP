<script setup>
const items = [
  { id: 1, name: 'Кружка', material: 'Фарфоровая', price: '23' },
  { id: 2, name: 'Кастрюля', material: 'Керамическая', price: '105' },
  { id: 3, name: 'Тарелка', material: 'Стеклянная', price: '15' },
]
</script>

<template>
    <div class="w-full overflow-x-auto">
      <!-- Для мобильных - вертикальная карточка -->
      <div class="block md:hidden space-y-4">
        <div v-for="item in items" :key="item.id" class="bg-white dark:bg-gray-800 rounded-lg shadow p-4">
          <div class="grid grid-cols-2 gap-2">
            <div class="font-bold text-gray-600 dark:text-gray-400">ID:</div>
            <div>{{ item.id }}</div>
            <div class="font-bold text-gray-600 dark:text-gray-400">Имя:</div>
            <div>{{ item.name }}</div>
            <div class="font-bold text-gray-600 dark:text-gray-400">Материал:</div>
            <div>{{ item.material }}</div>
            <div class="font-bold text-gray-600 dark:text-gray-400">Цена:</div>
            <div>{{ item.price }}</div>
          </div>
        </div>
      </div>
  
      <!-- Для десктопа - горизонтальная таблица -->
      <div class="hidden md:block">
        <div class="flex flex-col border border-gray-300 dark:border-gray-700 w-full">
          <div class="flex bg-gray-100 dark:bg-gray-800">
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center font-bold">ID</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center font-bold">Имя</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center font-bold">Материал</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center font-bold">Цена</div>
          </div>
          <div v-for="item in items" :key="item.id" class="flex">
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center">{{ item.id }}</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center">{{ item.name }}</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center">{{ item.material }}</div>
            <div class="flex-1 p-3 border border-gray-200 dark:border-gray-700 text-center">{{ item.price }}</div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
