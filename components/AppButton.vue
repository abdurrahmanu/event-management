<template>
    <p class="bg-[#783ead] hover:bg-[#432361] hover:scale-[96%] h-fit cursor-pointer text-white py-3 px-6 rounded-md text-[16px] w-fit">{{ text }}</p>
</template>

<script lang="ts" setup>
const props = defineProps({
    text: String
})
</script>