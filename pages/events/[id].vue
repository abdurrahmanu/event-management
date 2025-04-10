<template>
  <div class="p-[64px] py-[170px] relative">
    <div class="max-w-[1311px] w-[100%]">
      <img :src="imageUrl" alt="" class="rounded-[20px] max-h-[500px] w-full object-cover" />
    </div>

    <div class="pt-12 text-[24px] font-medium">{{ title }}</div>

    <main class="flex-col lg:flex-row justify-between">
      <section class="lg:w-[67%] max-w-[875px]">
        <div class="text-[16px] font-light">
          <p class="">{{ date }} {{ time }}</p>
          <p>{{ address }}</p>
          <p>{{ organizer.name }}</p>
        </div>

        <div class="text-[16px] font-light pt-6">
         <p class="font-medium">Event description</p> 
         <p class="text-justify lg:text-auto">{{ description }}</p>
        </div>

        <div class="lg:block flex justify-between items-center">
          <div class="pt-6 pb-10">
            <p class="font-medium text-[16px]">Ticket Pricing</p>
            <div class="flex gap-4">
              <div>
                <p class="text-[20px] font-medium">Single</p>
                <p class="text-[16px] text-[#9B51E0]">N5000</p>
              </div>
              <div>
                <p class="text-[20px] font-medium">Pair</p>
                <p class="text-[16px] text-[#9B51E0]">N9000</p>
              </div>        
             </div>
          </div>
  
          <BaseButton text="Buy Now" />
        </div>
      </section>


      <section class="lg:w-[31%] max-w-[100%] relative">
        <div>
          <p class="text-[16px] font-medium">Contact Organizers</p>
          <div>
            <div></div>
            <div></div>
            <div></div>
          </div>
        </div>
        <div>
          <p>Directions</p>
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