<template>
    <div class="max-h-[488px] m-auto lg:m-0 md:max-w-[60%] lg:max-w-0 max-w-[75%] min-w-[230px] lg:min-w-full relative shadow-md shadow-gray-300 rounded-[20px]">
        <div class="w-[100%] h-fit">
            <img :src="event.imageUrl" class="h-[170px] md:h-[240px] w-[100%] inline-block rounded-t-[20px]" width="100%" alt="">
        </div> 
        <div class="p-6 lg:space-y-5 space-y-3">
            <div class="lg:text-[16px] text-[14px]">
                <p>{{ event.title }}</p>
                <p class="text-gray-700">{{ event.date }} . {{ event.time }}</p>
            </div>
            <p class="max-h-[80px] h-[36px] md:h-[60px] overflow-clip lg:h-[80px] text-[12px] md:text-[14px]">{{ event.description.length > 270 ? event.description.substring(0, 200) + '...' : event.description }}</p>
            <NuxtLink :to="goToEvent">
                <div class="flex items-center cursor-pointer py-[2px] px-2 gap-1 hover:ring w-fit rounded-full">
                    <p class="text-[#432361]">View details</p>
                    <NuxtImg src="/arrow-top-right.svg" class="w-3" alt=""/>
                </div>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
  event: Object
});

const goToEvent = computed(() => `/events/${props.event.id}`)
</script>