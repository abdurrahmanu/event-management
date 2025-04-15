<template>
    <div class="text-[#432361] z-[2] fixed top-0 left-0 w-full py-0 md:py-[50px]">
        <div class="max-w-[1312px] md:w-[90%] w-full m-auto relative">
            <div class="top-0 bottom-0 left-0 right-0 absolute opacity-60 bg-white md:rounded-[20px]"></div>
            <div class="max-w-[1312px] items-center m-auto w-full flex-col justify-between p-6 rounded-[20px] relative bg-transparent">
                <div class="flex items-center justify-between w-full">
                    <Logo />
                    <nav>
                        <ul class="lg:flex hidden md:gap-6 gap-3 p-2 text-[14px] xl:text-[16px] font-medium">
                            <li v-for="(link, index) in links" :key="index"><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" :to="link.path">{{ link.name }}</NuxtLink></li>
                        </ul>
                    </nav>
                    <div class="flex items-center gap-4 text-[16px]">
                        <div><NuxtLink to="/sign" class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1">Login</NuxtLink></div>
                        <NuxtLink to="/sign"><AppButton text="Sign Up"/></NuxtLink>
                    </div>
                </div>
                <nav class="lg:hidden">
                    <ul class="flex md:gap-6 gap-3 p-2 pt-3 m-auto w-fit text-[13px] font-medium">
                        <li v-for="(link, index) in links" :key="index"><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" :to="link.path">{{ link.name }}</NuxtLink></li>
                    </ul>
                </nav>
            </div>
        </div>
    </div>
</template>

<script setup>
const links = ref([
    { name: 'Discover', path: '/' },
    { name: 'About Us', path: '/about' },
    { name: 'FAQs', path: '/faq' },
    { name: 'Contact Us', path: '/contact' }
])
</script>