<template>
  <NuxtLink :class="$style.button" :to="$props.to">
    <slot />
  </NuxtLink>
</template>

<script lang="ts">
export default defineComponent({
  props: {
    to: {
      type: String,
      default: '',
    },
  },
})
</script>

<style lang="postcss" module>
.button {
  @apply flex items-center w-auto rounded-md bg-customBlue hover:bg-blue-600 px-5 text-center text-base font-medium shadow-md duration-300 h-8 sm:h-10;
}
</style>
