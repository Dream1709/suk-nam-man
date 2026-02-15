<template>
   <div>
    <Navbar />
    <div class=" tw-text-5xl tw-font-bold tw-text-emerald-800 tw-pt-10 tw-text-bold tw-text-center">
    User page
    </div>
 
    <div class=" tw-flex tw-justify-center tw-pt-10">
    <Button label="ดึงข้อมูลผู้ใช้" @click="getUserList" />
    </div>
    
    <div class=" tw-grid tw-grid-cols-3 tw-gap-4 tw-px-20 tw-pt-10">
        <!--forloop-->
        <div v-for="item in users" :key="item.id">
        <div class=" tw-border tw-border-primary tw-bg-primary-bg tw-rounded-xl tw-p-5 tw-h-full"
        >
        <div class=" tw-flex">
            <img src="/public/image/woman-with-long-brown-hair-pink-shirt_90220-2940.avif" alt="woman" class=" tw-flex ">
        </div>
        <div class=" tw-text-md tw-text-secondary">{{ item.name }} <br/></div>
        <div class=" tw-text-md tw-text-black">{{ item.email }} <br/></div>
        <div class=" tw-text-md tw-text-black">
        {{ item.address.street }} <br/>
            {{ item.address.suite }} <br/>
            {{ item.address.city }} <br/>
            {{ item.address.zipcode }} <br/>
        </div>
        
        </div>
    </div>
   </div>
   </div>
</template>
 
<script lang="ts" setup>
import type { st } from 'vue-router/dist/router-CWoNjPRp.mjs';
 
interface User{
    id: number;
    name: string;
    email: string;
    address : {
        street: string;
        suite: string;
        city: string;
        zipcode: string;
    };
}
const users = ref<User[]>([]);
 
import axios from 'axios';
import { ref } from 'vue';
 
const getUserList = async () => {
     try {
          const response = await axios.get(
      "https://jsonplaceholder.typicode.com/users",
     );
      //console.log(response.data);
      users.value = response.data;
    } catch (error) {
      console.error("Error fetching user data" , error);
    }   
};
 
 
</script>
 
<style></style>