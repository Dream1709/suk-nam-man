<template>
  <div>
    <navbar/>

    <div class="tw-flex tw-flex-col tw-items-center tw-justify-center tw-h-[80vh] tw-text-center">
        
        <img src="/image/woman-with-long-brown-hair-pink-shirt_90220-2940.avif" alt="Woman" class="tw-w-64 tw-h-auto tw-mb-6 tw-rounded-lg"/>
        <h1 class="tw-text-6xl tw-font-bold tw-mb-5">
            Welcome to {{ name }}'s Blog
        </h1>
        <p class="tw-text-lg tw-mb-8 tw-text-gray-600">
            age: {{ age }} years old
        </p>
        
        <Button/>
    </div>
  </div>
</template>
<script setup lang="ts">

const name = 'Apiruk'
const age = 20

</script>


