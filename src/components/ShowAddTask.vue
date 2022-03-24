<script setup>
import Calendar from './Calendar.vue';
const value = new Date();
</script>


<template>
<div class="w-full h-40">
    <h2 class="text-xl font-['Proxima_Nova'] w-full text-center">New Task</h2>
    <Calendar class="w-full"/>
        <div class="text-left m-3 text-lg mt-0 formed">
            <label for="title" class="block pt-4">Title:</label>
            <input type="text" id="title" placeholder="Design for home page" class="mb-3 w-full"/>
            <label for="desc" class="block mt-2">Description:</label>
            <textarea id="desc" placeholder="What do you need to do?" rows="3" cols="30" class="border-l-[3px] border-green-400 placeholder:text-2xl placeholder:pt-[22px] resize-none pl-2 h-21 mt-2"/>
            <label for="notes" class="block mt-4">Notes:</label>
            <input type="text" id="notes" placeholder="Urgent" class="mb-4 w-full"/>
        </div>
        <button class="bg-[#2c82e0] rounded text-white text-center mt-3 font-medium uppercase w-64 h-12">Add Your Task</button>
</div>
</template>

