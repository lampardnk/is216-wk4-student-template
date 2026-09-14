<script setup>
    import { ref } from 'vue'

    const width = ref(200)
    const height = ref(200)
    const myImg = ref('/assets/me.png')
    const imageAttributes = ref({
        src: '/assets/me.png',
        alt: 'People outdoors',
        width: 200,
        height: 200
    })
</script>

<template>
    <img v-bind:src="myImg" alt="People outdoors" v-bind:width="width" v-bind:height="height">
    <img v-bind="imageAttributes">
</template>
