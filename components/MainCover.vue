<template>
        <div class="bg-[url(/main.png)] bg-cover w-full relative h-[640px] flex items-center justify-center pt-[50px]">
            <div class="flex xl:flex-row flex-col-reverse gap-y-10 justify-between items-center absolute bottom-[82px] max-w-[1312px] w-[90%]">
                <p class="max-w-[531px] min-w-[350px] text-[32px] font-medium text-white">Ready to Rock? Discover the Hottest Events Here – Your Calendar's New Best Friend!</p>
                <div class="flex bg-white shadow-md text-[#4f4f4f] xl:p-[24px] p-[14px] text-[16px] rounded-[20px] items-center space-x-6">
                    <div class="relative">
                        <img src="/search1.svg" class="absolute z-[2] top-[50%] translate-y-[-50%] left-0 w-7" alt="">
                        <input type="text" placeholder="Search for an event" class="border-none px-8 outline-none text-[16px] w-[200px] h-[40px] bg-transparent" />
                    </div>
                    <Dropdown />
                    <BaseButton text="Search" />
                </div>
            </div>
        </div>
</template>