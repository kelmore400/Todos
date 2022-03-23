<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

import Datepicker from './components/Datepicker.vue'
import SelectTask from './components/SelectTask.vue'
</script>

<template>
<div class="w-1/4">
<h1 class="text-2xl font-bold text-gray-900 mb-8 mr-10">Todos App</h1>
  <SelectTask />
  <Datepicker />
</div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
