<template>
    <main-layout>
    <span class="table mx-auto">
        <img alt="Vue logo" src="../assets/logo.png">
    </span>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <lipsum></lipsum>
    </main-layout>
</template>

<script>
import MainLayout from '../layouts/Main.vue'
import HelloWorld from '../components/HelloWorld.vue'
import lipsum from '../components/lipsum.vue'
export default {
  components: {
    MainLayout,
    HelloWorld,
    lipsum
  }
}
</script>