<script setup>
import SelectTask from './SelectTask.vue'
import CreateNew from './CreateNew.vue'

const props = defineProps({
    toggle: {
      type: Boolean,
      default: false
    }
})
</script>

<template>
<div>
  <div class="relative pt-[6px] ml-[2px] w-full">
    <img src="src/assets/button.svg" v-if="!toggle" @click="toggle = !toggle" class="absolute top-2 ml-[12px] w-18 pt-[2px]"/>
    <SelectTask v-if="!toggle"/>
  </div>
  <div class="relative pt-[6px] w-full">
    <img src="src/assets/arrow.svg" v-if="toggle" @click="toggle = !toggle" class="absolute top-2 ml-[12px] w-18 pt-[4px]"/>
    <CreateNew v-if="toggle"/>
  </div>
</div>
</template>