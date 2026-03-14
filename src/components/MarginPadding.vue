<template>
  <div class="bg-gray-100 dark:bg-gray-800 p-4 md:p-8 rounded-lg">
    <h2 class="text-xl md:text-2xl font-bold mb-6 text-gray-800 dark:text-white">Демонстрация отступов Margin и Padding</h2>
    
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4 md:gap-6">
      <div class="bg-blue-600 rounded-lg p-4 md:p-6 min-h-[120px] md:min-h-[150px] flex flex-col items-center justify-center text-white font-medium shadow-lg">
        <span class="text-xs md:text-sm opacity-80 mb-2">Padding</span>
        <span class="text-xs opacity-70 text-center">внутренние отступы</span>
      </div>

      <div class="bg-emerald-600 rounded-lg p-4 min-h-[120px] md:min-h-[150px] flex flex-col items-center justify-center text-white font-medium shadow-lg border-2 border-emerald-300 m-2 md:m-4">
        <span class="text-xs md:text-sm opacity-80 mb-2 text-center">Margin + Padding</span>
        <span class="text-xs opacity-70 text-center">Внешние и внутренние</span>
      </div>

      <div class="bg-gradient-to-r from-amber-500 to-orange-500 rounded-lg p-4 min-h-[120px] md:min-h-[150px] flex flex-col items-center justify-center text-white font-medium shadow-lg mx-2 md:mx-6 my-1 md:my-2">
        <span class="text-xs md:text-sm opacity-80 mb-2 text-center">Padding по сторонам</span>
      </div>

      <div class="bg-gradient-to-b from-purple-500 to-purple-700 rounded-lg p-4 min-h-[120px] md:min-h-[150px] flex flex-col items-center justify-center text-white font-medium shadow-lg mx-2 md:mx-6 my-1 md:my-2">
        <span class="text-xs md:text-sm opacity-80 mb-2 text-center">Margin по бокам</span>
      </div>
    </div>
  </div>
</template>