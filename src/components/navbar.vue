<template>
    <nav class="sticky top-0 bg-lime-darker rounded-b text-black">
        <div class="relative flex items-center justify-between h-14">
            <div class="">
                <a class="inline-block mx-5" v-for="site in navSites" v-bind:key="site.url" :href=site.url>{{ site.name }}</a>
            </div>
            <div class="absolute inset-y-0 right-2 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
                <dark-mode-toggle></dark-mode-toggle>
            </div>
        </div>
    </nav>
</template>

<script lang="ts">
import darkModeToggle from "./darkModeToggle.vue"

export default {
    name: "navbar",
    props: ["navSites"],
    components:{
        darkModeToggle
    }
}
</script>