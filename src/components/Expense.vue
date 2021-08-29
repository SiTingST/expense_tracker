<template>
    <div class = "expense">
        <h3> 
        {{expense.text}} 
        <i @click="OnDelete(expense.id)" class="fas fa-times"></i>
        </h3>

        <p> {{expense.price}} </p>
    </div>
</template>

<script> 
export default {
    name: 'Expense',
    props: {
        expense: Object
    },
    methods: {
        OnDelete(id){
            this.$emit('delete-expense', id)
        },
    },
}
</script> 

<style> 

<style scope>
.fas {
  color: red;
}
.expense {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

.expense h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>