<template>
  <div class="text-3xl h-screen w-full flex justify-center items-center">
    <BaseAlert>
      <template #icon> <ExclamationTriangleIcon class="h-6 w-6" /> </template>
      <template #text> Você precisa estar logado para interagir </template>
    </BaseAlert>
  </div>
</template>

<script setup lang="ts">
import { ExclamationTriangleIcon } from '@heroicons/vue/24/outline'
</script>
