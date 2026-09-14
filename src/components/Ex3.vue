<script setup>
    import { ref } from 'vue'

    const loginOption = ref('username')
</script>

<template>
    <h1>Please select your login option</h1>
    <select v-model="loginOption">
        <option value="username">Username login</option>
        <option value="email">Email login</option>
    </select>

    <div v-if="loginOption === 'username'">
        <label>Username</label>
        <input placeholder="Enter your username">
    </div>
    <div v-else>
        <label>Email</label>
        <input type="email" placeholder="Enter your email">
    </div>
</template>

