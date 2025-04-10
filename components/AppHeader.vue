<template>
    <div class="text-[#432361] z-[2] fixed top-0 left-0 w-full py-[50px]">
        <div class="max-w-[1312px] w-[90%] m-auto relative">
            <div class="top-0 bottom-0 left-0 right-0 absolute opacity-60 bg-white rounded-[20px]"></div>
            <div class="max-w-[1312px] items-center m-auto w-full flex-col justify-between p-6 rounded-[20px] relative bg-transparent">
                <div class="flex items-center justify-between w-full">
                    <img src="/rendezvous.png" alt="" class="scale-[70%] md:scale-[80%] lg:scale-[100%]" />
                    <nav>
                        <ul class="lg:flex hidden gap-6 p-2 text-[16px] font-medium">
                            <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/">Discover</NuxtLink></li>
                            <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/about">About Us</NuxtLink></li>
                            <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/faq">FAQs</NuxtLink></li>
                            <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/contact">Contact Us</NuxtLink></li>
                        </ul>
                    </nav>
                    <div class="flex items-center gap-4 text-[16px]">
                        <div><NuxtLink to="/sign" class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1">Login</NuxtLink></div>
                        <NuxtLink to="/sign"><BaseButton text="Sign Up"/></NuxtLink>
                    </div>
                </div>
                <nav class="lg:hidden">
                    <ul class="flex gap-6 p-2 m-auto w-fit text-[16px] font-medium">
                        <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/">Discover</NuxtLink></li>
                        <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/about">About Us</NuxtLink></li>
                        <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/faq">FAQs</NuxtLink></li>
                        <li><NuxtLink class="hover:ring-[#432361] rounded-md px-2 py-1 hover:ring-1" to="/contact">Contact Us</NuxtLink></li>
                    </ul>
                </nav>
            </div>
        </div>
    </div>
</template>