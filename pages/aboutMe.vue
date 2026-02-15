<template>
    <div>
    <navbar/>

    <div class="tw-flex tw-flex-col tw-items-center tw-justify-center tw-h-[80vh] tw-text-center">
        
        <img src="/image/woman-with-long-brown-hair-pink-shirt_90220-2940.avif" alt="Woman" class="tw-w-64 tw-h-auto tw-mb-6 tw-rounded-lg"/>
        <h1 class="tw-text-6xl tw-font-bold tw-mb-5">
            Hi my name is {{ name }},Nice to meet you
        </h1>
        <p class="tw-text-lg tw-mb-8 tw-text-gray-600">
            i am {{ age }} years old
        </p>
        
        <div class="tw-flex tw-justify-center">
        <button class="tw-text-center tw-bg-slate-200 tw-rounded-lg tw-p-3 tw-px-10 hover:tw-scale-95 tw-mt-2" 
        @click="navigateTo('')">Button</button>
    </div>
    </div>
  </div>
</template>
<script setup lang="ts">

const name = 'Apiruk'
const age = 20
</script>

    
