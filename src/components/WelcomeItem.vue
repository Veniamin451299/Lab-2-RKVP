<template>
  <div class="item flex items-center gap-4 mt-8 relative">
    <i class="flex items-center justify-center w-8 h-8 md:w-12 bg-green-500 text-white font-bold text-base rounded-full border border-[var(--color-border)] z-10 flex-shrink-0">
      <slot name="icon"></slot>
    </i>
    
    <div class="details flex-1 ml-4 break-words">
      <h3 class="text-lg font-medium mb-2 text-[var(--color-heading)] break-words">
        <slot name="heading"></slot>
      </h3>
      <p class="break-words whitespace-normal">
        <slot></slot>
      </p>
    </div>
  </div>
</template>

<style scoped>
.item {
  display: flex;
  position: relative;
}
</style>