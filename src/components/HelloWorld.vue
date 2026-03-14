<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="greetings text-center md:text-left">
    <h1 class="green text-2xl md:text-3xl lg:text-4xl font-medium relative -top-2 md:-top-3">
      {{ msg }}
    </h1>
    <h3 class="text-base md:text-lg lg:text-xl mt-2">
      Это текст создан в целях получения знаний по
      <a href="https://vite.dev/" target="_blank" rel="noopener" class="text-green-500 hover:bg-green-500/20 px-1 rounded transition">Vite</a>
      +
      <a href="https://vuejs.org/" target="_blank" rel="noopener" class="text-green-500 hover:bg-green-500/20 px-1 rounded transition">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
}

h3 {
  font-weight: normal;
}

.green {
  color: hsla(160, 100%, 37%, 1);
}

a {
  text-decoration: none;
  transition: 0.4s;
}
</style>