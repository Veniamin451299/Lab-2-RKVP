<template>
  <div class="item flex ml-0 md:ml-20 relative">
    <div class="details flex-1 ml-0 md:ml-4">
      <h3 class="text-xl md:text-2xl font-bold mb-2 text-[var(--color-heading)]">
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.item {
  display: flex;
  position: relative;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  h3 {
    font-size: 1.5rem;
  }
}
</style>