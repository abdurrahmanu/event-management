<template>
    <LandingPageCover />
    <Events :showAllEvents="showAllEvents"/>
    <Categories @showAllEvents="showAllEvents = $event" />
</template>

<script setup>
const showAllEvents = ref(false)
const emit = defineEmits(['showAllEvents'])
</script>