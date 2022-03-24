<script setup>
// import { ref } from 'vue';
// const search = ref("");
// function searchedProducts() {
// console.log(search._value);
// }
const search = "";
console.log(search);
</script>
<template>
    <div class="relative">
        <input type="text" v-model="search" class="border rounded pl-[5px] w-32"/>
        <img src="src/assets/search.svg" class="absolute top-[3px] right-[28px]"/>
    </div>
</template>