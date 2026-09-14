<script setup>
    import { ref } from 'vue'

    const message = ref('Choose your favorite fruit:')
    const fruit1 = ref('apple')
    const fruit2 = ref('orange')
    const fruit3 = ref('peach')
</script>

<template>
    {{ message }}

    <label for=""> <input type="radio" name="fruit"> {{ fruit1 }} </label>
    <label for=""> <input type="radio" name="fruit"> {{ fruit2 }} </label>
    <label for=""><input type="radio" name="fruit"> {{ fruit3 }} </label>
</template>

<style scoped>
</style>
