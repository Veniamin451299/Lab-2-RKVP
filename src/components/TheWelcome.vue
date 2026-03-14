<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
import HeadTitle from './HeadTitle.vue'
</script>

<template>
  <div class="welcome-container w-full max-w-full overflow-hidden">
    <HeadTitle>
      <template #heading>
        Хронология образования
      </template>
    </HeadTitle>

    <div class="welcome-items relative w-full">
      <WelcomeItem class="first">
        <template #icon>
          <DocumentationIcon />
        </template>
        <template #heading>Завершить 1 курс обучения</template>
        Пройти период адаптации и получения основы основ.
      </WelcomeItem>

      <WelcomeItem>
        <template #icon>
          <ToolingIcon />
        </template>
        <template #heading>Завершить 2 курс</template>
        Определиться с языком программирования и углубиться в знаниях.
      </WelcomeItem>

      <WelcomeItem>
        <template #icon>
          <EcosystemIcon />
        </template>
        <template #heading>Завршить 3 курс</template>
        Оттачиваем нами выбранный стек знаний.
      </WelcomeItem>

      <WelcomeItem>
        <template #icon>
          <CommunityIcon />
        </template>
        <template #heading>Завершить 4 курс</template>
        Сдать все дипломные испытания и заняться поиском работы
      </WelcomeItem>

      <WelcomeItem>
        <template #icon>
          <SupportIcon />
        </template>
        <template #heading>Устроиться на работу</template>
        Найти хорошую вакансию на специалиста по вашей сфере деятельности, пройти собеседование, начать карьерный рост!
      </WelcomeItem>
    </div>
  </div>
</template>

<style scoped>
/* Дополнительные стили если нужны */
.welcome-items {
  position: relative;
}

@media (min-width: 1024px) {
  .welcome-items {
    margin-left: 0;
  }
}
</style>