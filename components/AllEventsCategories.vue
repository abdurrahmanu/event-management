<template>
  <div class="flex flex-col xl:flex-row py-[127px] px-[64px] gap-[40px]">
    <div class="pt-1 max-w-[400px] space-y-5 text-center xl:text-left lg:m-left mx-auto">
      <p class="text-[32px] font-normal">Discover a world of events just tailored for you.</p>
      <BaseButton text="View all events" class="lg:m-0 m-auto" />
    </div>
    
    <div class="flex gap-4 flex-wrap xl:justify-start justify-center w-full">
      <EventCategory v-for="(eventType, index) in eventTypes" :key="index" :eventType="eventType" />
    </div>
  </div>
</template>

<script lang="ts" setup>
const eventTypes = [ '/online.png', '/physical.png', '/hybrid.png' ]
</script>