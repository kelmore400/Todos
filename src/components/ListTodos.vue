<script>
export default {
    data() {
        return {
            tasks: [],
            descriptions: {},
            colors: ['#FF4355', '#0063FF', '#FBAA21']
        }
    },
    mounted() {
        fetch('https://jsonplaceholder.typicode.com/todos')
        .then(res => res.json())
        .then(data => this.tasks = data.slice(0, 5))
        .catch(err => console.log(err.message))
        fetch('https://jsonplaceholder.typicode.com/posts')
        .then(res => res.json())
        .then(data => this.descriptions = data.slice(0, 5))
        .catch(err => console.log(err.message))
    }
}
</script>
<template>
<div>
    <div v-for="(task, index) in tasks" :key="task.id" class="w-full">
        <div class="h-20 drop-shadow-sm rounded-md bg-white flex items-center justify-between m-4">
            <svg width="10" height="10" class="ml-3 mt-6 self-start">
                <circle v-if="task.completed" cx="5" cy="5" r="4" fill="#FF4355" />
                <circle v-else cx="5" cy="5" r="4" fill="#0063FF" />
                Sorry, your browser does not support inline SVG.
            </svg>
            <div class=" w-10/12">
            <h2 class="first-letter:uppercase normal-case text-lg font-['Proxima_Nova'] block truncate text-left">{{ task.title }}</h2>
            <h3 class="truncate text-sm text-left text-gray-400">2018/10/01  {{ descriptions[index].body }}</h3>
            </div>
            <div v-if="task.completed" class="ml-2 w-[4px] h-[72px]" style="background: url(src/assets/undone.svg)"></div>
            <div v-else class="ml-2 w-[4px] h-[72px]" style="background: url(src/assets/done.svg)"></div>
        </div>
    </div>
</div>
</template>
