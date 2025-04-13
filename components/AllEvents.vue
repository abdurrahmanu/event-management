<template>
    <div v-if="events" class="p-[64px] relative max-w-[1320px] mx-auto">
        <p class="flex lg:justify-between justify-center items-center pb-[50px]">
            <p class="text-[32px]">Trending events</p>
            <div class="items-center cursor-pointer hidden lg:flex rounded-full px-2 hover:ring gap-2">
                <p @click="viewAll = !viewAll" class="text-[#432361]">{{!viewAll ? 'View all trending events' : 'Show fewer trending events'}}</p>
                <img src="/arrow-top-right.svg" class="w-4" alt="">
            </div>
        </p>
        <div v-if="events.data" class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 gap-4 place-items-center">
            <!-- <p class="text-[32px] font-black xl:hidden block font-mono" @click="prev"><</p> -->
            <SingleEvent class="" v-for="(event, index) in events.data.allEvents" :event="event" :key="index" />
            <!-- <SingleEvent class="xl:hidden block" :event="events.data.allEvents[current]" /> -->
            <!-- <p class="text-[32px] font-black xl:hidden block font-mono" @click="next">></p> -->
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