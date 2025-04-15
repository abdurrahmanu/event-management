<script setup lang="ts">
import type { NuxtError } from '#app'

const props = defineProps({
  error: Object as () => NuxtError
})
</script>

<template>
  <div v-if="error.statusCode === 404" class="w-[500px] text-[32px] h-screen m-auto flex flex-col items-center justify-center text-center font-bold space-y-4">
    <p class="text-red-400">404</p>
    <p>Page not found</p>
    <NuxtLink to="/">
      <AppButton text="Go back home" class="w-[200px] m-auto" />
    </NuxtLink>
  </div>
</template>