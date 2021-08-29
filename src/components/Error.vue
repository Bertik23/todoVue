<template>
    <div class="grid justify-items-center">
        <h1 class="text-9xl">{{ code }}</h1>
        <h3 class="text-4xl">{{ summary }}</h3>
        <p>{{more}}</p>
    </div>
</template>

<script>
export default {
    name: "Error",
    props: ["code", "summary"]
}
</script>