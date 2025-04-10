<template>
    <div v-if="events" class="p-[64px] relative">
        <p class="flex lg:justify-between justify-center items-center pb-[50px]">
            <p class="text-[32px]">Trending events</p>
            <div class="flex items-center cursor-pointer">
                <p @click="viewAll = !viewAll" class="p-2 hidden lg:block text-[#432361]">{{!viewAll ? 'View all trending events' : 'Show fewer trending events'}}</p>
                <img src="/arrow-top-right.svg" class="w-5" alt="">
            </div>
        </p>
        <div v-if="events.data" class="flex xl:flex-wrap xl:justify-between items-center justify-center space-y-6 space-x-5 xl:space-x-0">
            <p class="text-[32px] font-bold xl:hidden block" @click="prev"><</p>
            <SingleEvent class="hidden xl:block" v-for="(event, index) in events.data.allEvents" :event="event" :key="index" />
            <SingleEvent class="xl:hidden block" :event="events.data.allEvents[current]" />
            <p class="text-[32px] font-bold xl:hidden block" @click="next">></p>
        </div>
    </div>
</template>

<script setup>
const viewAll = ref(false)
const current = ref(0)

const { data: events } = await useFetch('https://rendezvous-events.onrender.com/events')

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
</script> 