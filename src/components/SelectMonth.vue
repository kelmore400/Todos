<script setup>
import { v4 } from '../../node_modules/uuid';
const months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];
const current = new Date();
const currentMonth = current.getMonth();
</script>
<template>
    <select class="text-xl font-['Proxima_Nova'] w-32 text-center" v-model="months[currentMonth]">
        <option v-for="(month, v4) in months" :key="v4">{{month}}</option>
    </select>
</template>