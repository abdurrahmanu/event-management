<template>
    <div v-if="events" class="md:px-[64px] px-[30px] py-[30px] lg:py-[60px] relative">
        <div class="max-w-[1312px] mx-auto">
            <p class="flex lg:justify-between justify-center items-center pb-[50px]">
                <p class="text-[32px]">Trending events</p>
                <div class="items-center cursor-pointer hidden lg:flex rounded-full px-2 hover:ring gap-2">
                    <p @click="viewAll = !viewAll" class="text-[#432361]">{{!viewAll ? 'View all trending events' : 'Show fewer trending events'}}</p>
                    <NuxtImg src="/arrow-top-right.svg" class="w-4" alt=""/>
                </div>
            </p>
            <div v-if="events.data" class="lg:grid flex w-fit m-auto lg:grid-cols-1 lg:w-full lg:m-0 lg:grid-cols-2 xl:grid-cols-3 gap-6 place-items-center">
                <Event class="hidden lg:block" v-for="(event, index) in showData" :event="event" :key="index" />
                <div @click="prev" class="lg:hidden block w-7 h-10 flex items-center justify-center rounded-md ring hover:gray-400 hover:ring-2">
                    <NuxtImg class="w-5" src="/arrow-left.svg" alt=""/>
                </div>
                <Event class="lg:hidden block" :event="events.data.allEvents[current]" />
                <div @click="next" class="lg:hidden block w-7 h-10 flex items-center justify-center rounded-md ring hover:bg-gray-400 hover:ring-2">
                    <NuxtImg class=" w-5" src="/arrow-right.svg" alt=""/>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const viewAll = ref(false)
const current = ref(0)

const props = defineProps({
    showAllEvents: Boolean
})

const { data: events } = await useFetch('https://rendezvous-events.onrender.com/events')

const showData = computed(() => {
    if (viewAll.value) {
        return events.value.data.allEvents
    } else {
        return events.value.data.allEvents.slice(0, 3)
    }
})

const next = () => {
    if (current.value < events.value.data.allEvents.length - 1) {
        current.value++
    } else {
        current.value = 0
    }
}

const prev = () => {
    if (current.value > 0) {
        current.value--
    } else {
        current.value = events.value.data.allEvents.length - 1
    }
}

watch(() => props.showAllEvents, (newValue) => {
    viewAll.value = !viewAll.value
})
</script> 