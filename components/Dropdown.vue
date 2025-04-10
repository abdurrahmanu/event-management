<template>
    <div class="relative cursor-pointer flex justify-between items-center">
        <div @click="toggle = !toggle" class="rounded-[10px] w-[144px]">Categories</div>
        <div class="absolute top-[100%] shadow-sm shadow-gray-300 left-0 bg-white rounded-md z-[2]">
            <div v-if="toggle" class="hover:bg-slate-200 first:pt-5 last:pb-5 px-10 py-2 rounded-md transition-all duration-[200ms]" v-for="(selection, index) in selections" :key="index">{{ selection }}</div>
        </div>
        <img @click="toggle = !toggle" :class="[toggle ? 'rotate-[180deg]' : '']" src="/chevron-down.svg" alt="">
    </div>
</template>

<script lang="ts" setup>
const selections = ['All', 'Comedy', 'Religious', 'Tech', 'Health', 'Fitness', 'Sports', 'Education']
const toggle = ref(false)
const currentSelection = ref('All')
</script>