<template>
  <div class="text-3xl h-screen w-full flex justify-center items-center">
    <BaseAlert v-if="!logged">
      <template #icon> <ExclamationTriangleIcon class="h-6 w-6" /> </template>
      <template #text> Você precisa estar logado para interagir </template>
      <template #button>
        <BaseButton to="/login"> Fazer Login! </BaseButton>
      </template>
    </BaseAlert>
  </div>
</template>

<script setup lang="ts">
import { ExclamationTriangleIcon } from '@heroicons/vue/24/outline'

const logged = ref(false)
</script>
