<template>
  <div class="bg-neutral-700">
    <div class="select-none max-w-[1700px] m-auto bg-white bg-red-600">
       <NuxtLayout>
         <NuxtPage />
       </NuxtLayout>
     </div>
  </div>
</template>

<style>
@font-face {
  font-family: 'Gilroy';
  src: url('/path-to-fonts/Gilroy-Regular.woff2') format('woff2'),
       url('/path-to-fonts/Gilroy-Regular.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'Gilroy';
  src: url('/path-to-fonts/Gilroy-Bold.woff2') format('woff2'),
       url('/path-to-fonts/Gilroy-Bold.woff') format('woff');
  font-weight: bold;
  font-style: normal;
}

body {
  font-family: 'Gilroy', sans-serif;
}
</style>