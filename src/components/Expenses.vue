<template>
    <div :key="expense.id" v-for="expense in expenses">
        <Expense @delete-expense="$emit('delete-expense', expense.id)" :expense="expense" />
    </div>
</template>

<script>
import Expense from './Expense'

export default{
    name: 'Expenses',
    props:{
        expenses:Array
    },
    components: {
        Expense
    },
    emits:['delete-expense'], 
}

</script>