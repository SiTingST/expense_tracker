<template>
    <button @click ="onClick()" class ="btn"> Add Expense </button>
</template>

<script>
export default {
    name: 'Button',
    methods: {
        onClick() {
            console.log("click me")
        }
    }
}
</script> 