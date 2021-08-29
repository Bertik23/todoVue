<template>
    <main-layout>
        <p>Hello, how are you?</p>
    </main-layout>
</template>

<script>
import MainLayout from '../layouts/Main.vue'
export default {
  components: {
    MainLayout
  },
    data:() => ({
        navSites: [
        {
          name: 'Home',
          url: '/'
        },
        {
          name: "About",
          url: "/about"
        }
      ]
    })
}
</script>