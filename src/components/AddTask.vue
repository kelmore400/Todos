<script setup>
import ShowAddTask from './ShowAddTask.vue';
import VueCompositionAPI from '@vue/composition-api';
const props = defineProps({
    toggle: {
      type: Boolean,
      default: false
    }
  })
</script>

<template>
<div>
    <img src="src/assets/button.svg" @click="toggle = !toggle" class="ml-2 w-18 pt-[2px]"/>
    <t-modal v-model="toggle">hello world</t-modal>
    <!-- <ShowAddTask v-if="toggle"/> -->
</div>
</template>