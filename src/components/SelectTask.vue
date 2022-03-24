<script setup>
import { v4 } from '../../node_modules/uuid';
import SearchBtn from './SearchBtn.vue';
import SelectMonth from './SelectMonth.vue';
import ListTodos from './ListTodos.vue';
import ShowAddTask from './ShowAddTask.vue';
import SelectDate from './SelectDate.vue';
import VueCompositionAPI from '@vue/composition-api';

</script>


<template>
<div>
<div class="flex justify-between items-center m-2 ml-3 w-[360px]">
<SelectMonth />
<SearchBtn className="mr-2 relative w-32" />
</div>
<div class="flex">
<SelectDate />
</div>
<div class="flex">
<ListTodos />
</div>
</div>
</template>