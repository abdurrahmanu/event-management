<template>
  <div class="p-[64px] pt-[170px] pb-[120px] max-w-[1440px] m-auto relative">
    <div class="max-w-[1440px] m-auto w-[100%]">
      <img :src="imageUrl" alt="" class="rounded-[20px] max-h-[500px] w-full" />
    </div>
    <div class="py-12 text-[24px] font-medium">{{ title }}</div>

    <main class="flex-col lg:flex-row flex justify-between lg:space-y-0 space-y-10">
      <section class="lg:w-[66%] max-w-[875px]">
        <div class="text-[16px] font-light space-y-3">
          <div class="flex gap-10 items-center">
            <p class="flex items-center gap-2">
              <img class="w-6" src="/calendar.svg" alt="">
              {{ date }}
            </p>
            <p class="flex items-center gap-2">
              <img class="w-6" src="/time.svg" alt="">
              {{ time }}
            </p>
          </div>
          <p class="flex items-center gap-2">
            <img class="w-6" src="/location.svg" alt="">
            {{ address }}
          </p>
          <p class="flex items-center gap-2">
            <img class="w-6" src="/user.svg" alt="">
            {{ organizer.name }}
          </p>
        </div>

        <div class="text-[16px] font-light pt-14 space-y-7">
         <p class="font-medium">Event description</p> 
         <p class="text-justify lg:text-auto">{{ description }}</p>
        </div>

        <div class="lg:block flex sm:justify-between justify-start flex-col lg:flex-row">
          <div class="pt-6 pb-10 space-y-5 lg:space-y-10">
            <p class="font-medium text-[16px]">Ticket Pricing</p>
            <div class="flex gap-10 flex-col sm:flex-row">
              <div class="space-y-2">
                <p class="text-[20px] font-medium">Single</p>
                <p class="text-[16px] text-[#9B51E0]">NGN 5,000</p>
              </div>
              <div class="space-y-2">
                <p class="text-[20px] font-medium">Pair</p>
                <p class="text-[16px] text-[#9B51E0]">NGN 9,000</p>
              </div>        
             </div>
          </div>
  
          <AppButton text="Buy now" />
        </div>
      </section>

      <section class="lg:w-[31%] max-w-[100%] relative">
        <div class="space-y-6">
          <p class="text-[16px] font-medium">Contact Organizers</p>
          <div class="flex items-center gap-4">
            <img class="w-8" src="/mail.svg" alt="">
            <img class="w-8" src="/twitter.svg" alt="">
            <img class="w-8" src="/insta.svg" alt="">
          </div>
        </div>
        <div class="space-y-6 pt-14">
          <p class="text-[16px] font-medium">Directions</p>
          <div class="w-full bg-blue-400">
            <img src="/location.png" class="w-[100%]" alt="">
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
const route = useRoute()
let id = route.params.id

const { data: eventsData } = await useFetch(`https://rendezvous-events.onrender.com/events/${id}`)
const {date, address, author, description, imageUrl, price, title, time, lat, long, category, country, organizer} = eventsData.value.data.event
</script>

<style>

</style>