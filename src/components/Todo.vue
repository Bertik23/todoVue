<template>
    <h1 class="text-3xl">Todo:</h1>
    <div class="grid gap-y-1">
    <todo-box>Make a todo in <a href="https://vuejs.org">Vue.js</a>.</todo-box>
    <todo-box v-for="todoitem in todoItems" v-bind:key="todoitem" :text="todoitem.text" :toggled="todoitem.toggled">{{ todoitem.html }}</todo-box>
    </div>
    <todo-add/>
</template>

<script>
import TodoBox from "../components/TodoBox.vue"
import TodoAdd from "../components/TodoAdd.vue"

export default {
    components: {
        TodoBox,
        TodoAdd
    },
    props:["todoItems"]
}
</script>