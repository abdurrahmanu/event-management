<template>
    <div class="rounded-lg scale:[0.8] relative xl:scale-[1] bg-red-300 hover:scale-[1.05] transition-all duration-[200ms] cursor-pointer relative overflow-hidden">
        <NuxtImg :src="eventType" class="min-w-[300px] md:min-w-[350px] lg:min-w-[400px]" alt=""/>
    </div>
</template>

<script setup>
const props = defineProps({
    eventType: String
})
</script>