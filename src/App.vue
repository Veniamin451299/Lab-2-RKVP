<script setup>
import FlexCards from './components/FlexCards.vue';
import GridCards from './components/GridCards.vue';
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import ColorsCards from './components/ColorsCards.vue';
import Typography from './components/Typography.vue';
import BackgroundsCards from './components/BackgroundsCards.vue';
import BorderCards from './components/BorderCards.vue';
import MarginPadding from './components/MarginPadding.vue';
import SizeCards from './components/SizeCards.vue';
import ThemeToggle from './components/ThemeToggle.vue';
</script>

<template>
  <div class="min-h-screen bg-white dark:bg-gray-900 transition-colors duration-300 w-full">
    <!-- Header start -->
    <header class="flex flex-col md:flex-row items-center justify-between gap-4 p-4 md:p-6
     border-b border-gray-200 dark:border-gray-700 w-full">
     <div class="flex flex-col md:flex-row items-center gap-4 w-full md:w-auto">
      <img alt="Vue logo" class="logo w-20 h-20 md:w-24 md:h-24 lg:w-32 lg:h-32 rounded-full border-4 border-green-500" 
             src="./assets/images/pepe.jpg" />
        
        <div class="wrapper text-center md:text-left">
          <HelloWorld msg="Антипов Вениамин" />
        </div>
     </div>

      <div class="theme-toggle-container">
        <ThemeToggle />
      </div>
    </header>
<!-- Header end -->

<!-- Main start -->
<main class="w-full px-4 md:px-6 lg:px-8 py-6 space-y-8">
  <div class="max-w-7xl mx-auto">
      <!-- Welcome selection -->
      <section class="w-full">
        <TheWelcome />
      </section>

      <!-- Components cards selection -->
      <section class="space-y-8">
        <!-- Flex cards -->
        <div id="fcard" class="fcard-container w-full overflow-x-auto">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Flex Cards</h2>
          <FlexCards />
        </div>

        <!-- Grid cards -->
        <div id="gcard" class="gcard-container w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Grid Cards</h2>
          <GridCards />
        </div>

        <!-- Colors cards -->
        <div id="colorcard" class="color-cards w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Colors</h2>
          <ColorsCards />
        </div>

        <!-- Typography -->
        <div id="Tgcard" class="tg-cards w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Typography</h2>
          <Typography />
        </div>

        <!-- Backgrounds cards -->
        <div id="BGcard" class="BGcards w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Backgrounds</h2>
          <BackgroundsCards />
        </div>

        <!-- Borders cards -->
         <div id="BRDcard" class="BRDcards w-full">
          <h2 class="text-xl font-bold mb-4 text-gray-800 dark:text-white">Borders</h2>
          <BorderCards />
         </div>

        <!-- Margin / Padding cards -->
        <div id="MarPad" class="mar-pad w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Margin & Padding</h2>
          <MarginPadding />
        </div>

        <!-- Size Cards -->
        <div id="sizecard" class="size-cards w-full">
          <h2 class="text-xl md:text-2xl font-bold mb-4 text-gray-800 dark:text-white">Size Cards</h2>
          <SizeCards />
        </div>
      </section>
    </div>
  </main>
<!-- Main end -->
  </div>
</template>

<style scoped>
.container {
  width: 100vw;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.theme-toggle-container {
  margin-left: auto;
}

@media (min-width: 1920px) {
  .container {
    max-width: 1920px;
  }
}

@media (min-width: 1280px) {
  .container {
    max-width: 1280px;
  }
}



@media (min-width: 640px) {
  .container {
    max-width: 640px;
  }
}

@media (min-width: 768px) {
  .container {
    max-width: 768px;
  }
}

@media (min-width: 1024px) {
  .container {
    max-width: 1024px;
  }
}

</style>
