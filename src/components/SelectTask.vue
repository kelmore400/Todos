<script setup>
import { v4 } from '../../node_modules/uuid';
import AddTask from './AddTask.vue';
import SearchBtn from './SearchBtn.vue';
import SelectMonth from './SelectMonth.vue';
</script>


<template>
<div class="flex justify-between items-center m-2">
<AddTask />
<SelectMonth />
<SearchBtn className="mr-2 relative w-32"/>
</div>
</template>