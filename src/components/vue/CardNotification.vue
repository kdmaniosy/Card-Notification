<script setup>
import { ref } from 'vue';
const counter = ref(0)
function decrement() {
    if (counter.value > 0) {
        counter.value--
    }
}
function increment(){
    counter.value++
}
</script>

<template>
    <div class="flex-col bg-slate-200 rounded py-8 px-6 w-96 items-center flex shadow-md">
    <div class="relative">
        <img class="size-32 rounded-full" src="https://metamorphosiscounselling.com/wp-content/uploads/2018/04/square-profile-pic.jpg" alt="">
        <div v-show="counter>0" class="absolute right-0 top-0 flex justify-center items-center size-6 rounded-full bg-red-500 text-white ">
            {{ counter }}
        </div>
       
    </div>
    <p v-if="counter>0">Tienes nuevos mensajes 😁</p>
    <p v-else="">Nadie te habla 🥲</p>



<div class="flex justify-around w-24 mt-6">
<button @click="decrement" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">-</button>
{{ counter }}
<button @click="increment" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">+</button>
</div>
    </div>

</template>