<script setup>
    import { ref } from 'vue'

    // part 1
    const id = ref('demo')
    const id2 = ref('demo2')
    const blueBox = ref(true)
    const blueBtn = ref(true)

    // part 2
    const activeColor = ref('red')
    const redBtn = ref(true)

    // implement methods below 
    // part 1
    function changeColor() {
        if (blueBox.value) {
            blueBox.value = false
            blueBtn.value = false
        } else {
            blueBox.value = true
            blueBtn.value = true
        }
    }

    // part 2
    function changeTextColor() {
        if (activeColor.value == "blue") {
            activeColor.value = "red"
            redBtn.value = true
        } else { 
            activeColor.value = "blue"
            redBtn.value = false
        }
    }

</script>

<template>
    <div id="part1">
        <div
            id="demo"
            :class="{ blueBox: blueBox, redBox: !blueBox }"
        >
            div ID : {{ id }}
        </div>

        <button
            type="button"
            :class="{ 'btn-primary': blueBtn, 'btn-danger': !blueBtn }"
            v-on:click="changeColor"
        >
            Change Color
        </button>
    </div>

    <div id="part2">
        <div
            :id="id2"
            :style="{ color: activeColor }"
        >
            div ID : {{ id2 }}
        </div>

        <button
            type="button"
            :class="{ 'btn-danger': redBtn, 'btn-primary': !redBtn }"
            v-on:click="changeTextColor"
        >
            Change Text Color
        </button>
    </div>
</template>

<style scoped>
    .redBox {
            background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    .btn-primary {
        background-color: blue;
        color: white;
    }
    .btn-danger {
        background-color: red;
        color: white;
    }
    #demo {
        color: white;
    }
</style>
