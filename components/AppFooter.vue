<template>
  <div class="bg-[#432361] xl:px-[64px] px-[20px] md:px-[30px]">
    <div class="flex flex-col lg:space-y-0 sticky bottom-[-100%] space-y-10 lg:flex-row justify-between text-white py-[56px] text-[16px] max-w-[1312px] mx-auto font-normal">
      <div class="max-w-[340px] mx-auto lg:m-0 text-center lg:text-left">
        <p class="text-[32px] font-medium">rendezvous</p>
        <!-- font - gilroy regular -->
        <p class="font-light">Your personal event sherpa: Curating Awesome one click at a time</p> 
      </div>
      <div class="flex justify-between lg:m-0 gap-[30px] lg:gap-[80px] flex-col md:flex-row text-center lg:text-left">
        <div class="space-y-4">
          <p class="font-medium">Feature</p>
          <div class="space-y-2">
            <p class="hover:underline cursor-pointer">Event discovery</p>
            <p class="hover:underline cursor-pointer">Ticketing</p>
          </div>
        </div>
        <div class="space-y-4 text-center lg:text-left">
          <p class="font-medium">Company</p>
          <div class="space-y-2">
            <p class="hover:underline cursor-pointer"><NuxtLink to="/about">About Us</NuxtLink></p>
            <p class="hover:underline cursor-pointer"><NuxtLink to="/faq">FAQs</NuxtLink></p>
            <p class="hover:underline cursor-pointer"><NuxtLink to="/">Careers</NuxtLink></p>
            <p class="hover:underline cursor-pointer"><NuxtLink to="/">Support</NuxtLink></p>
          </div>
        </div>
        <div class="space-y-4 text-center lg:text-left">
          <p class="font-medium cursor-pointer text-center lg:text-left">Contact Us</p>
          <div class="max-w-[240px] m-auto lg:m-0 text-center lg:text-left space-y-2">
            <p class="hover:underline cursor-pointer"><NuxtLink to="/">info@events.com</NuxtLink></p>
            <p class="hover:underline cursor-pointer"><NuxtLink to="/">+234 701 345 6789</NuxtLink></p>
            <p>Race course, 8/9 Marina, Onikan, Lagos Lagos, 4aa Force Rd Lagos Island 102273, Lagos</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>