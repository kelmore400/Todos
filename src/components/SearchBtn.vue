<script setup>
const search = "";
console.log(search);
</script>
<template>
    <div class="relative">
        <input type="text" v-model="search" class="border rounded pl-[5px] w-32"/>
        <img src="src/assets/search.svg" class="absolute top-1 right-1"/>
    </div>
</template>