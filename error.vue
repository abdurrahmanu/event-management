<script setup lang="ts">
import type { NuxtError } from '#app'

const props = defineProps({
  error: Object as () => NuxtError
})

const handleError = () => clearError({ redirect: '/' })
</script>

<template>
  <div class="w-[500px] text-[32px] m-auto font-bold space-y-4">
    <h2 class="text-center">{{ error.statusCode }}</h2>
    <img src="/404.png" class="w-[200px]" alt="">
    <NuxtLink to="">
      <BaseButton text="Go back home" class="w-[200px] m-auto" />
    </NuxtLink>
  </div>
</template>