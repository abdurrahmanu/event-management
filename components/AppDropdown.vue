<template>
    <div class="relative cursor-pointer flex justify-between items-center hover:text-black hover:bg-blue-200 px-2 rounded-md py-1">
        <div @click="toggle = !toggle" class="rounded-[10px] w-[144px]">Categories</div>
        <div class="absolute top-[100%] shadow-sm shadow-gray-500 left-[50%] translate-x-[-50%] bg-white rounded-md z-[2]">
            <div v-if="toggle" class="hover:bg-slate-200 first:pt-5 last:pb-5 px-10 py-2 rounded-md transition-all duration-[200ms] text-[14px]" v-for="(option, index) in options" :key="index">{{ option }}</div>
        </div>
        <img @click="toggle = !toggle" :class="[toggle ? 'rotate-[180deg]' : '']" src="/chevron-down.svg" alt="">
    </div>
</template>

<script lang="ts" setup>
const toggle = ref(false)

const props = defineProps({
    options: Array
})
</script>