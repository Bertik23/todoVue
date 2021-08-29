<template>
    <form>
        <input type="text" v-model="newTodoText">
        <input type="submit" @click.prevent="addTodo">
    </form>
</template>

<script>
export default {
    setup(){
        const newTodoText = ""
        return { newTodoText }
    },
    methods: {
        addTodo(){
            var currentItems = JSON.parse(window.localStorage.getItem("todoItems"))
            currentItems.push({id: currentItems.length, text:this.newTodoText, toggled:false})
            window.localStorage.setItem("todoItems", JSON.stringify(currentItems))
            console.log(this.$parent, this.$parent.$parent.todoItems)
            this.$emit("todoChanged")
            //this.$parent.todoItems.push({id: currentItems.length, text:this.newTodoText, toggled:false})
        }
    }
}
</script>