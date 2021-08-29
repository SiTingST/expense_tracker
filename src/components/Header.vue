<template>
    <header>
        <h1> Expense Tracker </h1>
        <Button/>
    </header>
</template>

<script> 
import Button from './Button'

export default {
    name: 'Header',
    components: {
        Button
    }
}

</script>

<style scooped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom:20px;
    }
</style>