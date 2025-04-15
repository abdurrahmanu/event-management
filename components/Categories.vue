<template>
  <div class="flex flex-col xl:flex-row py-[30px] lg:py-[50px] px-[30px] lg:px-[64px] gap-[40px]">
    <div class="flex flex-col xl:flex-row lg:py-[127px] py-[50px] gap-[40px] max-w-[1312px] mx-auto">
      <div class="pt-1 max-w-[400px] space-y-5 text-center xl:text-left lg:m-left mx-auto">
        <p class="md:text-[32px] font-normal text-3xl">Discover a world of events just tailored for you.</p>
        <AppButton 
          text="view all events" 
          class="xl:m-0 m-auto" 
          @click="emit('showAllEvents')" 
        />
      </div>
      <div class="flex gap-6 flex-wrap xl:justify-start justify-center w-full">
        <Category v-for="(eventType, index) in eventTypes" :key="index" :eventType="eventType" />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const emit = defineEmits(['showAllEvents']);
const eventTypes = [ '/online.png', '/physical.png', '/hybrid.png' ]
</script>