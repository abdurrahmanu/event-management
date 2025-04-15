<template>
    <LandingPageCover />
    <ClientOnly >      
        <Events :showAllEvents="showAllEvents"/>
        <Categories @showAllEvents="showAllEvents = $event" />
    </ClientOnly>
</template>

<script setup>
const showAllEvents = ref(false)
const emit = defineEmits(['showAllEvents'])
</script>