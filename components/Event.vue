<template>
    <div class="max-h-[488px] m-auto lg:m-0 lg:max-w-0 max-w-[400px] min-w-[250px] lg:min-w-full relative shadow-md shadow-gray-300 rounded-[20px]">
        <div class="w-[100%] h-fit">
            <img :src="event.imageUrl" class="h-[200px] md:h-[240px] w-[100%] inline-block rounded-t-[20px]" width="100%" alt="">
        </div> 
        <div class="p-6 space-y-5">
            <div>
                <p class="text-[16px]">{{ event.title }}</p>
                <p class="text-gray-700">{{ event.date }} . {{ event.time }}</p>
            </div>
            <p class="max-h-[80px] h-[80px]">{{ event.description.length > 270 ? event.description.substring(0, 200) + '...' : event.description }}</p>
            <NuxtLink :to="goToEvent">
                <div class="flex items-center cursor-pointer py-[2px] px-2 gap-1 hover:ring w-fit rounded-full">
                    <p class="text-[#432361]">View details</p>
                    <img src="/arrow-top-right.svg" class="w-3" alt="">
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