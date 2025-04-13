<template>
    <div class="rounded-lg h-[240px] scale:[0.8] xl:scale-[1] hover:scale-[1.05] transition-all duration-[200ms] cursor-pointer relative overflow-hidden">
        <img :src="eventType" alt="" width="100%" height="100%">
    </div>
</template>

<script setup>
const props = defineProps({
    eventType: String
})
</script>