<script setup>
    import { ref } from 'vue'

    const myImg = ref('/assets/me.png')
    const width = ref(300)
    const height = ref(200)
</script>

<template>
    <img
        v-bind:src="myImg"
        v-bind="{ width, height }"
        alt="People outdoors"
    >
</template>
