<template>
  <div :class="$style.bg">
    <TheHeader />
    <slot />
  </div>
</template>

<script setup lang="ts">
import { TheHeader } from '#components'

useHead({
  title: 'Julius',
  link: [
    {
      rel: 'icon',
      type: 'image/x-icon',
      href: '/favicon.ico',
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com',
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.gstatic.com',
      crossorigin: 'anonymous',
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Inter:wght@400;500&display=swap',
      crossorigin: 'anonymous',
    },
  ],
})
</script>

<style lang="postcss" module>
:root {
  font-family: 'Inter', sans-serif;
  scroll-behavior: smooth;
}
::selection {
  background: #f4f4f5;
  color: #121214;
}
::-moz-selection {
  background: #f4f4f5;
  color: #121214;
}

@media (min-width: 1024px) {
  * {
    scrollbar-width: auto;
    scrollbar-color: #1c56b8 #ffffff10;
  }

  *::-webkit-scrollbar {
    width: 5px;
  }

  *::-webkit-scrollbar-track {
    background: #ffffff10;
  }

  *::-webkit-scrollbar-thumb {
    background-color: #1c56b8;
    border-radius: 12px;
    border: 0px none #fff;
  }
}

.bg {
  @apply text-white;
  background: radial-gradient(
      90.69% 50% at 50% 100%,
      rgba(28, 86, 184, 0.25) 0%,
      rgba(0, 0, 0, 0) 100%
    ),
    #121214;
}
</style>
