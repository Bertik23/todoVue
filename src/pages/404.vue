<template>
  <main-layout>
    <Error code=404 summary="Page not found."/>
  </main-layout>
</template>

<script>
import MainLayout from '../layouts/Main.vue'
import Error from "../components/Error.vue"
export default {
  components: {
    MainLayout,
    Error
  }
}
</script>