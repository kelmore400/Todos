<script setup>
import ListTodos from './ListTodos.vue';
import '@vuepic/vue-datepicker/dist/main.css';
import { v4 } from '../../node_modules/uuid';
import { ref } from 'vue';

const months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];
const week = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'];
const current = new Date();
const currentDay = current.getDay();
const currentDate = current.getDate();
const currentMonth = current.getMonth();
console.log(currentDate);
console.log(currentMonth);
var startDay = currentDate;
if(currentDay != 1){
  startDay = currentDate - currentDay + 1;
}
var daysInWeek = [];
function createWeek(startDay) {
  for(var i = 0; i < 7; i++) {
    if(startDay == 29 && currentMonth == 1 
    || startDay == 30 && currentMonth == 1 
    || startDay == 31 && currentMonth == 3 
    || startDay == 31 && currentMonth == 5
    || startDay == 31 && currentMonth == 8
    || startDay == 31 && currentMonth == 10
    || startDay == 32 ){
      startDay = 1;
    }
    daysInWeek[i] = startDay;
    startDay += 1;
  }
}
createWeek(startDay);
</script>

<template>
<div>
  <div class="grid grid-cols-7 grid-flow-row gap-3 m-4 mr-4 mb-6 text-center text-lg items-center font-['Helvetica']">
    <div v-for="(days, index) in week" :key="days.v4" class="text-center text-base text-gray-400" :class="index == currentDay - 1 ? 'blue':''">{{days}}</div>
    <div v-for="dates in daysInWeek" :key="dates.v4" class="text-center" :class="dates == currentDate ? 'dateInWeek':''">{{dates}}</div>
  </div>
  <div>
    <ListTodos />
  </div>
  </div>
</template>

<style scoped>
.dateInWeek {
  background-color: #2E66E7;
  padding-top: 3px;
  font-size: 20px;
  color: white;
  font-weight: bold;
  width: 34px;
  height: 34px;
  border-radius: 17px;
}
.blue {
  color: #2E66E7;
}
a {
  color: #42b983;
}
</style>
