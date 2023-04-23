<template>
  <section :class="$style.bg">
    <BaseContainer>
      <nav :class="$style.navbar">
        <a href="/" alt="Logo Julius" :class="$style.logo">
          <span class="sr-only">Julius</span>
          Julius
        </a>

        <BaseButton href="/logar" v-if="!logged">Logar</BaseButton>
      </nav>
    </BaseContainer>
  </section>
</template>

<script setup lang="ts">
const logged = ref(false)
</script>

<style lang="postcss" module>
.bg {
  @apply fixed top-0 inset-x-0 bg-clip-padding backdrop-filter backdrop-blur-md bg-opacity-[0.02] bg-white;
}

.navbar {
  @apply flex items-center justify-between min-h-[60px] px-4;
}

.logo {
  @apply flex items-center h-8 sm:h-10 text-black bg-white rounded-md px-6 font-black uppercase;
}
</style>
