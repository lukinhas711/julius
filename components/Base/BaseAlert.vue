<template>
  <section :class="$style.modal">
    <slot name="icon"></slot>
    <p :class="$style.text">
      <slot name="text"></slot>
    </p>
  </section>
</template>

<style lang="postcss" module>
.modal {
  @apply bg-clip-padding backdrop-filter backdrop-blur-md bg-opacity-[0.02] bg-white rounded-md border-b border-white border-opacity-10 flex flex-col justify-center items-center gap-5 h-1/3 w-1/3 px-4 text-center;
}

.text {
  @apply text-lg;
}
</style>
