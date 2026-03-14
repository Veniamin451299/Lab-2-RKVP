<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// system state
const theme = ref('system') // 'light', 'dark' or 'system'

// func for theme application
const applyTheme = (newTheme) => {
  // safe choice user
  if (newTheme === 'system') {
    localStorage.removeItem('theme')
    // check system settings
    if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  } else {
    localStorage.setItem('theme', newTheme)
    if (newTheme === 'dark') {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  }

  theme.value = newTheme
}

// listen changes of system theme
const mediaQuery = window.matchMedia('(prefers-color-scheme: dark)')
const handleSystemThemeChange = (e) => {
  if (theme.value === 'system') {
    if (e.matches) {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  }
}

onMounted(() => {
  // define the current theme at loading
  const savedTheme = localStorage.getItem('theme')
  
  if (!savedTheme) {
    theme.value = 'system'
    if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  } else {
    theme.value = savedTheme
    if (savedTheme === 'dark') {
      document.documentElement.classList.add('dark')
    } else {
      document.documentElement.classList.remove('dark')
    }
  }

  // add listener of system theme changes
  mediaQuery.addEventListener('change', handleSystemThemeChange)
})

// clear listener when unmounted
onUnmounted(() => {
  mediaQuery.removeEventListener('change', handleSystemThemeChange)
})
</script>

<template>
  <!-- Адаптивный контейнер -->
  <div class="flex flex-col sm:flex-row items-stretch sm:items-center gap-2 p-2 sm:p-4 bg-gray-100 dark:bg-gray-800 rounded-lg w-full sm:w-auto">
    
    <!-- Вариант 1: Для мобильных - иконки + текст, для десктопа - только иконки (компактно) -->
    <button
      @click="applyTheme('light')"
      class="flex-1 sm:flex-none px-3 sm:px-4 py-2 rounded-lg transition-colors text-sm sm:text-base"
      :class="theme === 'light'
        ? 'bg-blue-500 text-white'
        : 'bg-gray-200 text-gray-700 dark:bg-gray-700 dark:text-gray-300 hover:bg-gray-300 dark:hover:bg-gray-600'"
    >
      <!-- На мобильных показываем иконку + текст -->
      <span class="inline sm:hidden">☀️ Светлая</span>
      <!-- На десктопе только иконку (компактно) -->
      <span class="hidden sm:inline">☀️</span>
    </button>

    <button
      @click="applyTheme('dark')"
      class="flex-1 sm:flex-none px-3 sm:px-4 py-2 rounded-lg transition-colors text-sm sm:text-base"
      :class="theme === 'dark' 
        ? 'bg-blue-500 text-white' 
        : 'bg-gray-200 text-gray-700 dark:bg-gray-700 dark:text-gray-300 hover:bg-gray-300 dark:hover:bg-gray-600'"
    >
      <span class="inline sm:hidden">🌙 Темная</span>
      <span class="hidden sm:inline">🌙</span>
    </button>

    <button
      @click="applyTheme('system')"
      class="flex-1 sm:flex-none px-3 sm:px-4 py-2 rounded-lg transition-colors text-sm sm:text-base"
      :class="theme === 'system' 
        ? 'bg-blue-500 text-white' 
        : 'bg-gray-200 text-gray-700 dark:bg-gray-700 dark:text-gray-300 hover:bg-gray-300 dark:hover:bg-gray-600'"
    >
      <span class="inline sm:hidden">💻 Системная</span>
      <span class="hidden sm:inline">💻</span>
    </button>
  </div>
</template>