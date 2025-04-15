<template>
    <p class="bg-[#783ead] hover:bg-[#432361] hover:scale-[96%] h-fit cursor-pointer text-white py-2 px-4 md:py-3 md:px-6 rounded-md md:text-[16px] text-[14px] w-fit">{{ text }}</p>
</template>

<script lang="ts" setup>
const props = defineProps({
    text: String
})
</script>