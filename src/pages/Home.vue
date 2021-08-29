<template>
    <main-layout>
    <span class="table mx-auto">
        <img alt="Vue logo" src="../assets/logo.png">
    </span>
    <Todo :todoItems="todoItems" @todoChanged="this.$forceUpdate"/>
    <lipsum></lipsum>
    </main-layout>
</template>

<script>
import MainLayout from '../layouts/Main.vue'
import Todo from "../components/Todo.vue"

export default {
  components: {
    MainLayout,
    Todo
  },
  created() {
    this.todoItems = JSON.parse(window.localStorage.getItem("todoItems"))
  }
}
</script>