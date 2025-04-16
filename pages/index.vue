<template>
    <div class="min-h-[100dvh]">
        <LandingPageCover />
        <ClientOnly >      
            <Events :showAllEvents="showAllEvents"/>
            <Categories @showAllEvents="showAllEvents = $event" />
        </ClientOnly>
    </div>
</template>

<script setup>
const showAllEvents = ref(false)
const emit = defineEmits(['showAllEvents'])
</script>